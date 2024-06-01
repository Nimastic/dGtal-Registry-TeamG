The `dGtal-Registry-TeamG` repository is a project focused on a blockchain-based content registry and licensing system. It uses a Next.js frontend and a backend built with Node.js, Truffle, and Solidity for smart contract deployment. The system allows users to register digital assets, manage licenses, and verify ownership using Ethereum blockchain and Metamask for transactions. The backend handles contract compilation, deployment, and interactions through Ganache for a local blockchain environment.

For more details, you can check this repository [here](https://github.com/Nimastic/dGtal-Registry-TeamG).

The Devpost for the project can be found [here](https://devpost.com/software/dgtal-registry?ref_content=my-projects-tab&ref_feature=my_projects).


## FRONTEND

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

### Prerequisites
Ensure you have Node.js installed on your machine.

Metamask Chrome extension installed 


## Getting Started

Clone the repository:
   ```bash
   git clone https://github.com/darren159/g.git
   cd g
   npm install
   nvm use 18.17.0
   npm run dev

Alternate running of the development server:

npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

On the frontend, click on Add Ganache Network and connect Wallet

use a private key from the Ganache Wallet Account to log in

In the upload tab, you can register new assets and upload files, login into Metamask to finalise your actions

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## BACKEND

### Prerequisites
Ensure you have the following installed:
- Node.js
- npm
- Truffle
- Ganache (Download the GUI version from Google)

on Ganache:

Click New Workspace (Ethereum)

Add Project 

Locate truffle-config.json from Lifehack root directory

Click Start



Clone the Repository:
`git clone [https://github.com/yourusername/blockchain-image-protection.git](https://github.com/junnengsoo/lifehack.git)`

Navigate to the Project Directory:
`cd lifehack`

Install Dependencies:
`npm install`

Compile Contracts:
`truffle compile`

Run Migrations:
`truffle migrate --reset`

```bash
Compiling your contracts...
===========================
> Compiling ./contracts/ContentRegistry.sol
> Compiling ./contracts/LicenseManager.sol
> Artifacts written to /Users/jerielchan/Documents/lifehack/build/contracts
> Compiled successfully using:
   - solc: 0.8.0+commit.c7dfd78e.Emscripten.clang

Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.


Starting migrations...
======================
> Network name:    'development'
> Network id:      5777
> Block gas limit: 6721975 (0x6691b7)


2_deploy_contracts.js
=====================

   Replacing 'ContentRegistry'
   ---------------------------
   > transaction hash:    0x9ec0e779334e542745c59ce6d2bf3cbb62dfd2554c4804f4eb46a16ea1ef5644
   > Blocks: 0            Seconds: 0
   > contract address:    0x91563e319f5b40a9D072e761d5A186243576E139
   > block number:        1
   > block timestamp:     1717210116
   > account:             0xB0232A2A760Aa07fa73A70dC7967e69bd3b2d87a
   > balance:             99.99564718825
   > gas used:            1289722 (0x13adfa)
   > gas price:           3.375 gwei
   > value sent:          0 ETH
   > total cost:          0.00435281175 ETH


   Replacing 'LicenseManager'
   --------------------------
   > transaction hash:    0xc02f052c668e189d774a5fa48684ddb11b5d463b2ceb47b819ee9f3e49dcb842
   > Blocks: 0            Seconds: 0
   > contract address:    0x829b935F3bfE971f8C4a7Ca471acad532e0fa7da
   > block number:        2
   > block timestamp:     1717210117
   > account:             0xB0232A2A760Aa07fa73A70dC7967e69bd3b2d87a
   > balance:             99.98354561469284518
   > gas used:            3658722 (0x37d3e2)
   > gas price:           3.30759581 gwei
   > value sent:          0 ETH
   > total cost:          0.01210157355715482 ETH

   > Saving artifacts
   -------------------------------------
   > Total cost:     0.01645438530715482 ETH

Summary
=======
> Total deployments:   2
> Final cost:          0.01645438530715482 ETH

```

In Ganache GUI's Contracts Tab, ContentRegistry and LincenseManager are now deployed.

Interacting with Contracts

Open Truffle Console:
`truffle console`

Get Contract Instances:
`const ContentRegistry = await artifacts.require("ContentRegistry").deployed();`
`const LicenseManager = await artifacts.require("LicenseManager").deployed();`

Call Contract Methods:
```bash
// Example: Register content
await ContentRegistry.registerContent("contentHash", { from: accounts[0] });

// Example: Get content details
const details = await ContentRegistry.getContentDetails("contentHash");
console.log(details);
```

