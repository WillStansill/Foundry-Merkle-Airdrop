# 🌳 Merkle Tree Airdrop - Secure & Gas-Efficient Token Distribution

## Overview
The **Merkle Tree Airdrop** is a secure and gas-efficient smart contract implementation for distributing ERC20 tokens to a predefined list of recipients. By leveraging **Merkle Trees**, this project ensures efficient proof verification, reducing gas costs and preventing unnecessary storage writes. 

This implementation follows industry best practices for **off-chain whitelist management** and **on-chain Merkle root verification**, making it scalable and highly optimized.

## 🚀 Features
- **Merkle Tree-Based Verification**: Utilizes a Merkle root to verify eligibility without storing recipient data on-chain.
- **Gas Optimization**: Eliminates unnecessary writes to the blockchain, minimizing transaction costs.
- **Flexible Token Distribution**: Allows recipients to claim their allocated tokens with a single transaction.
- **Security & Reliability**: Implements thorough testing with Foundry, including fuzz testing and invariant checks.

## 🛠 Tech Stack
- **Smart Contract Language**: Solidity
- **Testing & Deployment**: Foundry, Forge
- **Merkle Tree Generation**: JavaScript (Node.js)
- **Blockchain**: Ethereum (Mainnet/Testnet/Local Development)

## 📂 Project Structure
```
MerkleAirdrop/
│── src/                 # Solidity smart contracts
│── scripts/             # Deployment & Merkle root generation
│── test/                # Foundry test cases
│── utils/               # Merkle tree construction
│── README.md            # Project documentation
```

## 🏗 Deployment Guide
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/merkle-airdrop.git
cd merkle-airdrop
```
### **2️⃣ Install Dependencies**
```bash
npm install
forge install
```
### **3️⃣ Generate Merkle Root**
Before deploying, construct the Merkle tree from the recipient list:
```bash
node scripts/generateMerkleRoot.js
```
This outputs a `merkleRoot` that will be used in the smart contract.

### **4️⃣ Deploy the Contract**
```bash
forge script script/Deploy.s.sol --rpc-url <NETWORK_RPC> --private-key <YOUR_PRIVATE_KEY> --broadcast
```

### **5️⃣ Claim Airdrop**
Eligible recipients can claim their tokens by submitting a Merkle proof:
```solidity
airdropContract.claimAirdrop(index, account, amount, proof);
```

## 🔬 Testing & Security
- **Unit Testing**: Ensures contract correctness with Foundry's high-performance test framework.
- **Fuzz Testing**: Identifies edge cases by generating randomized inputs.
- **Invariant Testing**: Verifies that unauthorized claims cannot be executed.

## 🌍 Future Enhancements
- **On-Chain Merkle Root Updates**: Enable dynamic recipient lists.
- **Batch Claims**: Optimize gas fees for multiple claims.
- **Multi-Token Airdrops**: Expand support to multiple ERC20 tokens.

## 📬 Contact
📧 Email: willstansill@gmail.com  
💼 LinkedIn: [linkedin.com/in/will-stansill](https://linkedin.com/in/will-stansill)  
🐙 GitHub: [github.com/yourusername](https://github.com/yourusername)  

---
**Efficient, secure, and scalable airdrops made simple.** 🔥
