# VertexPulse

Built for Base

VertexPulse is a Base-focused repository created to observe network state, wallet connectivity, and RPC consistency across Base environments using official Coinbase tooling.

The project acts as a lightweight inspection layer rather than a full application, making it suitable for repeated Base infrastructure checks.

## Supported Networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

## What VertexPulse Does

Primary file: app/vertexPulse.ts

At runtime, the application:
- Initializes an OnchainKit provider bound to the selected Base chain
- Displays wallet connection UX
- Uses Viem to perform read-only RPC calls:
  - chainId
  - latest block number
  - native ETH balance for a provided address
- Outputs Basescan explorer references for visibility

## Repository Structure

app/  
- vertexPulse.ts  
  React entry point combining OnchainKit wallet components with Base RPC reads.

Common supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Libraries

OnchainKit  
Wallet UI components and Base-first primitives  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base JSON-RPC reads  

## Installation & Usage

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies and run using a standard React/Vite or Next.js development server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## License

MIT License

## Author

GitHub: https://github.com/roadmap-cedilla  
Public contact (email): roadmap-cedilla-0k@icloud.com   
Public contact (X): https://x.com/a_m3090  

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract "contract" address:  
0x4be8d2ebe1be8fa37d950c19a507c7365e8ac22d  

Deployment and verification:
- https://sepolia.basescan.org/address/0x4be8d2ebe1be8fa37d950c19a507c7365e8ac22d  
- https://sepolia.basescan.org/0x4be8d2ebe1be8fa37d950c19a507c7365e8ac22d/0#code  

Contract "control" address (optional):  
0x4c01751f30d5906e46581a8a281465dc8a1d2dc8  

Deployment and verification:
- https://sepolia.basescan.org/address/0x4c01751f30d5906e46581a8a281465dc8a1d2dc8  
- https://sepolia.basescan.org/0x4c01751f30d5906e46581a8a281465dc8a1d2dc8/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
