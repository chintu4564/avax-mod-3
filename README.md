# CustomToken

## Overview

This repository contains a Solidity smart contract for a custom ERC-20 token named `CustomToken`. The contract is built on the Ethereum blockchain and extends the functionality of the OpenZeppelin ERC-20 implementation. The token includes features such as minting, burning, and transferring tokens, and it is initially owned by the deploying address.

## Smart Contract Details

### ERC-20 Standard

The `CustomToken` contract complies with the ERC-20 standard, providing basic functionalities such as transferring tokens, querying balances, and approving token transfers.

### Token Ownership

The contract includes a `TokenOwner` variable, representing the address that initially owns the token. The `onlyTokenOwner` modifier ensures that certain operations can only be performed by the owner.

### Events

The contract emits three events:

1. **MintedTokens**: Triggered when new tokens are minted. It provides information about the beneficiary and the volume of tokens minted.

2. **BurnedTokens**: Triggered when tokens are burned. It provides information about the burner and the volume of tokens burned.

3. **TransferredTokens**: Triggered when tokens are transferred. It provides information about the sender, beneficiary, and the volume of tokens transferred.

### Constructor

The contract constructor initializes the token with a given name and symbol. It sets the `TokenOwner` to the deploying address and mints an initial supply of 0 tokens.

## Functions

### `mintTokens`

The `mintTokens` function allows the token owner to mint new tokens and assign them to a specified beneficiary. This function can only be called by the token owner.

### `burnTokens`

The `burnTokens` function allows any address to burn a specified volume of their own tokens, effectively reducing the total supply.

### `transferTokens`

The `transferTokens` function allows any address to transfer tokens to another address. It provides flexibility for users to transfer their tokens to different accounts.

## Getting Started

To deploy and interact with the `CustomToken` contract, follow these steps:

1. Deploy the contract to an Ethereum-compatible blockchain.
2. Interact with the contract using a compatible Ethereum wallet or through a decentralized application (DApp).

## Example Usage

Below is an example of how to interact with the contract using a hypothetical scenario:

1. Deploy the `CustomToken` contract.
2. Mint 100 tokens to address `0x123...`.
   ```solidity
   mintTokens(0x123..., 100);
   ```

3. Burn 50 tokens from the sender's address.
   ```solidity
   burnTokens(50);
   ```

4. Transfer 30 tokens from the sender's address to address `0x456...`.
   ```solidity
   transferTokens(0x456..., 30);
   ```
# Contact 
chintubasha186@gmail.com

