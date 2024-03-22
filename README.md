### README

This repository contains a Solidity smart contract named **Multisig** and a React web application to interact with the smart contract.

### Multisig Smart Contract

The Solidity smart contract `Multisig.sol` implements a simple multisignature wallet. It allows multiple approvers to create and approve transfers of Ether to other addresses. Key features of the smart contract include:

- **approvers**: An array of addresses representing the approvers.
- **quorum**: The minimum number of approvals required for a transfer to be executed.
- **Transfer struct**: Defines a transfer with an ID, amount, recipient address, number of approvals, and a flag indicating whether the transfer has been sent.
- **transfers mapping**: Maps transfer IDs to Transfer structs.
- **nextId**: Tracks the ID for the next transfer.
- **approvals mapping**: Tracks which approvers have approved each transfer.

### React Web Application

The React web application `App.js` provides a user interface to interact with the Multisig smart contract. Key features of the application include:

- **Balance Display**: Displays the current balance of the Multisig contract.
- **Create Transfer Form**: Allows an approver to create a new transfer by specifying the amount and recipient address.
- **Approve Transfer Section**: Displays information about the current transfer awaiting approval, including its ID, amount, and number of approvals. If the current user has not yet approved the transfer, they can approve it by clicking the "Submit" button.

### Getting Started

To run the React application locally, follow these steps:

1. Clone the repository to your local machine.
2. Install dependencies by running `npm install` in the project directory.
3. Start the React development server with `npm start`.
4. Open your browser and navigate to `http://localhost:3000` to view the application.

### Smart Contract Deployment

Before using the web application, ensure that the Multisig smart contract has been deployed to a supported Ethereum network, and update the `contract` variable in `App.js` with the contract address.

### Dependencies

- Solidity ^0.5.2
- React
- Web3.js

### License

This project is licensed under the MIT License. Feel free to use, modify, and distribute the code as needed.
