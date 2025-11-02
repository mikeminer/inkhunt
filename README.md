# 🦑 Kraken Hunt — Ink Mission Control

A high-performance **stress-testing DApp** for smart-contract deployments on **Ink Mainnet** (EVM L2 by Kraken • OP Stack).

Send a **burst of deploy transactions** to a Factory contract (`deployChild()`) to benchmark:

✅ Throughput  
✅ Latency  
✅ Sequencer responsiveness  
✅ Gas consumption  
✅ Success/failure rates  

> ⚠️ **Access is gated** — users must hold **The Citadel Spaceship** NFT on **Base** to unlock the deployment engine.

---

### 🚀 Live DApp

👉 **https://mikeminer.github.io/inkhunt/**

> Requires a browser wallet (e.g. MetaMask / Rabby)  
> Network: **Ink Mainnet**  
> NFT Ownership Check: **Base Mainnet**

---

### 🧠 How It Works

Each launch round triggers multiple calls to your Factory contract:

```solidity
function deployChild() external payable returns (address);
You control:

Number of transactions

Sequential or parallel mode

Delay between calls (ms)

ETH value forwarded per deploy

Real-time telemetry includes:

Metric	Description
Total Tx	All attempted transactions
Success vs Failures	On-chain confirmation
Gas Used	Sum of confirmed receipts
Execution time	Per-TX + full session
Progress Tracking	New tier every 50 successes

CSV export included ✅

🎯 Use Cases
Stress testing a Factory deployment system

Measuring sequencer performance on Ink L2

Load testing RPC endpoints

Benchmarking gas costs for contract creations

Performance comparisons between chains

🛡 NFT Gating (strict)
Ownership detection performed read-only on Base RPC:

makefile
Copia codice
NFT: The Citadel Spaceship
Contract: 0x67e2f3a9b7fe9979e3b4a5e557b59e9c93331c4f
Chain: Base Mainnet
If user does not hold the NFT:

Controls remain locked

A banner links to OpenSea marketplace

✅ No private key or sensitive data is ever transmitted externally.

🧩 Tech Stack
HTML + Vanilla JS

ethers.js v6

OP Stack-compatible contracts

Wallet-based or private key-based execution modes

Responsive UI • sci-fi theme ("Kraken Hunt")

⚙️ Local Development
bash
Copia codice
git clone https://github.com/mikeminer/inkhunt
cd inkhunt
# open index.html locally OR
python3 -m http.server 8080
Ensure your wallet is on:

yaml
Copia codice
Network: Ink Mainnet
Chain ID: 57073
RPC (example): https://rpc-gel.inkonchain.com
Currency: ETH
✅ Status Roadmap
Feature	Status
Ink Mainnet support	✅
Base NFT gating	✅
CSV Export	✅
Gas + latency metrics	✅
Auto network switch to Ink	🔜
Additional contract actions	🔜
Multi-wallet load balancing	🔜

⚠️ Disclaimer
This tool is for private testing & research only.
Do not use uncontrolled parallel execution on production funds.

Built for explorers who want to push the Ink network to its limits.
🦑 Hunt the Kraken — deploy at warp speed.
