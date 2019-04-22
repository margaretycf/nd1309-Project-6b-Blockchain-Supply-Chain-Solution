# Blockchain Developer Nanodegree Term 2

# Architect a Blockchain Supply Chain Solution - Part B

I implemented a supply chain Blockchain solution for the [Blockchain Developer Nanodegree Program Term 2 Project 6](https://classroom.udacity.com/nanodegrees/nd1309/parts/8ccccdaa-79a3-443a-a03f-00cacd0277b7/modules/47d6cc21-fafe-406e-8370-e5ba23875da8/lessons/da5331bc-e6ae-4372-b18a-71fa7cc77b67/project).

## The design UML diagrams of this solution 
### Activity Diagram
![Activity Diagram](diagrams/Activity_Diagram.png)

### Sequence Diagram
![Sequence Diagram](diagrams/Sequence_Diagram.png)

### State Diagram
![State Diagram](diagrams/State_Diagram.png)

### Class Diagram
![Class Diagram](diagrams/Class_Diagram.png)

## The implementation has the following subcontracts inheritance structure: 
```
contract AccessControl
contract Base is AccessControl
contract Core is Base
```
### AccessControl - Collection of Contracts: 
These contracts manage the various addresses and constraints for operations that can be executed only by specific roles.

There are 4 actors in a coffee supply chain:

- Farmer: The Farmer can harvest coffee beans, process coffee beans, pack coffee palettes, add coffee palettes, ship coffee palettes, and track authenticity.
- Distributor: The Distributor can buy coffee palettes and track authenticity.
- Retailer: The Retailer can receive coffee palettes and track authenticity.
- Consumer: The consumer can buy coffee palettes and track authenticity.

### Base - SupplyChain.sol: 
Tis defines the most fundamental code shared throughout the core functionality. This includes the main data storage, constants and data types, plus internal functions for managing these items.

### Core - Ownable.sol: 
It is the contract that controls ownership and transfer of ownership.

## Steps to run this project in development environment

Clone this repository:

```
git clone https://github.com/margaretycf/nd1309-Project-6b-Blockchain-Supply-Chain-Solution
```

### Launch Ganache locally
```
ganache-cli -m "enroll crazy just label faith garlic derive outer clerk recipe differ winter"
```

In a separate terminal window, Compile smart contracts:
```
truffle compile
```

Migrate smart contracts to the locally running blockchain, ganache-cli:
```
truffle migrate
```

Test smart contracts:
```
truffle test
```
All 10 tests should pass.

### Migrate to Rinkeby Network
```
truffle migrate --reset --network rinkeby
```

### Launch DApp
In a separate terminal window, launch the DApp:
```
npm run dev
```

Then run the DApp in browser - http://localhost:3000/

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

## Project Environment

- node version: v10.15.0
- Truffle version: v4.1.14
- web3 version: v0.20.3

## Project Results

### Deployed Contract Address:
https://rinkeby.etherscan.io/address/0xd0bd4df402345e8f15f9dd0e41112f972d5f6c31

### Transaction History
- Harvested - 0x6388510cd6dd37b0806bf0dae6cc586567e9d8c14bcfea8e7b69effbbf5e3aae
- Processed - 0x4345b4bfc9e0435e65c9de92ffa89426cc036415bdc487faf7db064cecdc1ee1
- Packed - 0x6ddf4a36558d34f99bcba94488d0780b26077cf0ed61905e6790ea55c9196333
- ForSale - 0xeb07e77c4cf9b5688d45b59ee57453e5c8f373c156315ae7cf9f67bfbe588459
- Sold - 0x1d3bfa6b7e7d1a5289971a5e71ec7fb270028593e5149a0b7d42fe6bbd39ebe6
- Shipped - 0x6fcc75f7b0bf3cc55441ef05c97bb1401d06560fcad6f1d9e9a875b62fa1be64
- Received - 0xfbd87887fa7378e8161b27ec3dc4fd505d5d0c3fc29ff3c3c370964f9848c449
- Purchased - 0x1d9f1de40fa59f37362b1c718890a226ee37378f47fe5d34007ad4ccded4d2f3