# new-NFT

---

# NFT Contract on Flow Blockchain

This repository contains a simple non-fungible token (NFT) contract written in Cadence for the Flow blockchain. NFTs are unique digital assets used for various purposes, such as digital art, collectibles, and more. This contract demonstrates the core concepts of creating, managing, and interacting with NFTs on Flow.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Code Overview](#code-overview)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Exploring the Contract](#exploring-the-contract)


## Prerequisites

Before you get started, ensure that you have the following prerequisites:

- Flow CLI: You'll need the Flow command-line interface to interact with the Flow blockchain.

## Code Overview

The NFT contract is designed to provide a basic understanding of NFT creation and management on the Flow blockchain. Here's an overview of the key components of the code:

- Import Statements: The contract imports the `NonFungibleToken` library from a specific address. This library provides the foundational functionality for NFTs.

- Contract Definition: The `CryptoPoops` contract inherits from the `NonFungibleToken` contract, extending its capabilities. It represents a collection of NFTs and provides functions to interact with them.

- Event Declarations: The contract declares three events: `ContractInitialized`, `Withdraw`, and `Deposit`. These events are used to notify external systems or users about specific actions within the contract.

- NFT Resource: The `NFT` resource represents a single NFT. It has properties like `id`, `name`, `favouriteFood`, and `luckyNumber`. The `init` function initializes these properties when a new NFT is created.

- Collection Resource: The `Collection` resource represents a user's collection of NFTs and implements several interfaces for NFT management.

- Functions in Collection Resource: Functions like `withdraw`, `deposit`, `getIDs`, `borrowNFT`, and `borrowAuthNFT` allow users to manage their NFTs within the collection.

- Minter Resource: The `Minter` resource is responsible for creating new NFTs. It provides functions to create NFTs with specified data.

- Initialization: The `init` function initializes the contract when it's deployed. It sets the `totalSupply` to 0, emits the `ContractInitialized` event, creates a `Minter` instance, and links a capability for the user's NFT collection.

- Transaction Script: The transaction script interacts with the contract to create and deposit NFTs. It borrows references to the user's `Minter` and `Collection` resources, creating the collection if it doesn't exist.

- Script for Querying NFT Data: The script allows external queries of NFT data. It borrows a reference to the user's collection, authenticates the reference, and fetches specific NFTs using their IDs.


## Usage

You can use this contract as a starting point to build more advanced NFT applications on the Flow blockchain. Here are some usage examples:

- Create your own NFT collection contract based on this code.
- Extend the contract with additional features and functionalities.
- Integrate this contract into a broader blockchain-based application.

## Exploring the Contract

To explore the contract in more detail, you can:

- Review the code in the `contracts` directory.
- Experiment with deployment and interaction using the Flow CLI.
- Read the comments and documentation within the code for further insights.

