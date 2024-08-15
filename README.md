# 💰 ERC20 & Vault Contracts README

Welcome to the **ERC20 & Vault Smart Contracts** repository! This documentation will guide you through understanding and using these contracts. Let's dive right in.

## 🚀 Overview

This project contains two primary smart contracts:

1. **ERC20 Contract** - A standard token contract that implements the ERC20 interface.
2. **Vault Contract** - A secure vault that allows users to deposit and withdraw ERC20 tokens.

### Key Features
- **ERC20 Contract**
  - Standard token functions like `transfer`, `approve`, `transferFrom`, etc.
  - Customizable parameters like `name`, `symbol`, and `decimals`.
  - Supports token minting and burning.

- **Vault Contract**
  - Users can securely deposit and withdraw ERC20 tokens.
  - Tracks individual user balances.
  - Ensures secure access control with role-based permissions.


## 🔍 ERC20 Contract Usage

### Deployment
- Customize your token by setting the `name`, `symbol`, `decimals`, and `initialSupply` during deployment.

### Interacting with the Token
- **Transfer Tokens:**
    ```solidity
    function transfer(address recipient, uint256 amount) public returns (bool)
    ```
    Transfer `amount` of tokens to `recipient`.

- **Approve Spending:**
    ```solidity
    function approve(address spender, uint256 amount) public returns (bool)
    ```
    Allow `spender` to withdraw from your account multiple times, up to the `amount`.

- **Check Balance:**
    ```solidity
    function balanceOf(address account) public view returns (uint256)
    ```
    Returns the token balance of a specific `account`.

## 🔐 Vault Contract Usage

### Deployment
- Deploy the Vault contract after the ERC20 contract deployment. Link it with the ERC20 token contract.

### Deposit & Withdraw Tokens
- **Deposit Tokens:**
    ```solidity
    function deposit(uint256 amount) public
    ```
    Deposits `amount` of tokens into the vault, increasing your balance.

- **Withdraw Tokens:**
    ```solidity
    function withdraw(uint256 amount) public
    ```
    Withdraws `amount` of tokens from the vault, decreasing your balance.

### Security & Access Control
- Only authorized users can perform certain administrative actions, ensuring secure access and control over the vault.

## 📄 Example Transactions

### Example: Depositing Tokens
```solidity
// Assuming the user has approved the vault to spend their tokens
vault.deposit(100 * (10 ** 18)); // Deposits 100 tokens to the vault
```

### Example: Withdrawing Tokens
```solidity
vault.withdraw(50 * (10 ** 18)); // Withdraws 50 tokens from the vault
``
### thank you 
