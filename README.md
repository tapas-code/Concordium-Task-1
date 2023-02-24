# Concordium: Task-1
Setting up the development environment.

##   Install Rust & Cargo

You must first install rustup, which sets up Cargo and Rust on your PC. Install rustup for your platform by going to [Rustup](https://rustup.rs/)
You should see something like the screenshot below after successfully installing Rust and Cargo on your system.

![RUST_Install](Screenshots/RUST_Install.png)

##   Install Wasm

Installing Wasm, which will be used for building contracts, requires copying and pasting this command into a terminal. <br />

_rustup target add wasm32-unknown-unknown_

![WASM_Install](Screenshots/WASM_Install.png)

Installing the Concordium software package is the next step. <br />
To download it, [click](https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#cargo-concordium-testnet) on this link. <br />
First, rename the cargo-concordium-v.x.x file to cargo-concordium. <br />
The tool should be placed in your PATH. <br />

![CheckPoint0](Screenshots/CheckPoint0.png)

##   Install Concordium Client

Concordium-client is a command line tool that is used in the tutorials for deployment, minting, and transfer. You can get it [here](https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#concordium-node-and-client-download-testnet). If the package has any version annotations, rename it to concordium-client.

[Install Concordium-Client](https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#concordium-node-and-client-download-testnet)

Use the following command to see if concordium-client can be launched: <br />
_concordium-client --help_

![CheckPoint](Screenshots/CheckPoint.png)

##   Check the installation and connect to the testnet node

You can connect to the public node with the following command:<br />
_concordium-client consensus status --grpc-port 10000 --grpc-ip node.testnet.concordium.com_

![PublicNode](Screenshots/PublicNode.png)


## Setting up Wallet

Your Concordium wallet is now necessary. Utilize the [Concordium Web Wallet](https://chrome.google.com/webstore/detail/concordium-wallet/mnnkpffndmickbiakofclnpoiajlegmg/related?hl=en-US). A 24-word secret recovery phrase is used by the Concordium Wallet for Web to protect your wallet. Ensure that you safeguard your 24-word secret recovery phrase and keep it in a safe location. <br />

Create an identity based on the Concordium testnet IP (illustrated below) and configure it to run on testnet with an account based on that identity. 
When choosing a Concordium testnet IP, you are not required to provide an ID in order to create an identity on the testnet. Only the testnet can use test identities.

To obtain 2000 CCDs for testing, use your account's Testnet faucet.

## Exporting and Importing Private Key

Click on the export button in the wallet which should download a <public key>.export file to your downloads folder

<p float="left">
  <img src="Screenshots/TestnetWallet.png" height="450">
  <img src="Screenshots/ExportKeys.png" height="450">
</p>


Now import the key using terminal by using the command shown below <br />
_concordium-client config account import <YOUR PUBLIC ADDRESS.export> --name <Your-Wallet-Name>_
  
<img src="Screenshots/ImportKeys.png">
