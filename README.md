# Solana Lending Protocol

A Solana-based lending protocol that allows users to deposit collateral and borrow tokens (such as USDC or SOL) based on their collateralized assets. The protocol uses real-time price feeds from **Pyth** and supports token transfers, interest calculations, and collateral management.

## Overview

This smart contract, written using the **Anchor framework**, enables the following:

- **Bank Setup**: Create a bank where users can deposit collateral and borrow funds.
- **User Initialization**: Allow users to initialize their accounts with collateral and borrow funds from the bank.
- **Borrowing**: Users can borrow tokens from the bank based on their collateralized assets.
- **Collateral Management**: The protocol calculates and tracks collateral values and borrowing limits based on dynamic price feeds.
- **Interest Calculation**: The system calculates accrued interest based on the deposited collateral over time.

The contract utilizes **Pyth** for price feeds and includes basic error handling and token transfers using the **anchor_spl** library.

## Features

- **Bank Initialization**: Allows for the creation of a bank that can manage multiple users, store collateral, and issue loans.
- **User Accounts**: Users can create an account linked to a specific mint (e.g., USDC or SOL) and begin interacting with the bank.
- **Collateralized Borrowing**: Users can borrow funds by locking their assets as collateral, with a liquidation threshold to protect the bank.
- **Real-Time Price Feeds**: Price data is provided by **Pyth**, ensuring accurate valuation of collateral.
- **Interest Rate Calculation**: Interest is applied to collateral over time, with accruals tracked and updated periodically.
- **Cross-Program Invocation (CPI)**: The contract interacts with the token program for transferring tokens and managing accounts.

