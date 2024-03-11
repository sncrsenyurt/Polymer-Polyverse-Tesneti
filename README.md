# Polymer Polyverse Testnet Guide

![polymer](https://pbs.twimg.com/media/GHrV-BVaUAA5qFd?format=jpg&name=medium)

## System Requirements:

**Ubuntu 22.04+**

NODE TYPE | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Polyverse | 2          | 2         | 40  |
  
  

**Required Updates and Installations**

```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt-get install -y ca-certificates curl gnupg
```
```bash
sudo mkdir -p /etc/apt/keyrings
```
```bash
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
```
```bash
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_${NODE_MAJOR}.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list
```
```bash
sudo apt-get update
```
```bash
sudo apt-get install -y nodejs
```


**Installing Git**

```bash
sudo apt-get install git
```


**Clone the Repository**
```bash
git clone https://github.com/sarox0987/polymerlab-ibc-app-solidity.git
```
```bash
cd polymerlab-ibc-app-solidity
```

**Optimism and Base Sepolia Faucets**

> You can use the faucet for [Optimism Sepolia](https://www.alchemy.com/faucets/optimism-sepolia) here.

> You can use the faucet for [Base Sepolia](https://www.alchemy.com/faucets/base-sepolia) here.

> Ensure that your test wallet has sufficient ETH by using these two faucets.

**Get Alchemy RPC**

> Go to the Alchemy website [here](https://alchemy.com/?r=b9d675bdc6edda35) and sign in with Gmail.

> Get the Public RPC for both Optimism and Base Sepolia.

> Go to the App section and click on "Create App";

> Choose Optimism and select Optimism Sepolia as the network. Add a name and description for the app and click on Create App.

> Repeat the same steps for Base Sepolia. In short, you should have two different RPCs.

> Click on the API Key button.

> Copy the API key in the first line to somewhere. Similarly, get an API Key for Base Sepolia and note it down.

**Get Metamask Private Key**

> Follow the steps in the image to get the private key of your Metamask wallet and note it down.

**Just Installation**

```bash
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to /usr/local/bin
```

**Forge Installation**

```bash
curl -L https://foundry.paradigm.xyz | bash
```
```bash
source /root/.bashrc
```
```bash
foundryup
```
```bash
forge build
```


**Edit the env file**

```bash
nano .env
```

> Add the private key you obtained from Metamask to the place marked as `PRIVATE_KEY_1`.

> For the places marked as `OP_ALCHEMY_API_KEY` and `BASE_ALCHEMY_API_KEY`, add the API keys you obtained from Alchemy for Optimism Sepolia and Base Sepolia respectively.

> After editing, save and exit by pressing Ctrl + X, then Y, and finally Enter.

**Install IBC Transfer and Contracts**

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
```bash
source ~/.bashrc
```
```bash
nvm install 18
```
```bash
nvm use 18
```
```bash
npm install
```

```bash
just install
```

```bash
just do-it
```
> You will get a similar result as below. Note down the links for both Optimism and Base.

**If You Encounter an Error**
```bash
npx hardhat clean
```
> After this, you can rerun the command `just do-it`.

**Getting the Polyverse Devs Discord Role**

> To get this role, first join the Discord channels. If you haven't joined yet, you can join [here](https://discord.gg/DEedJybQqG). Complete the Verify step, then in the `proof` channel, share a screenshot and links similar to those shared there to obtain the `Polyverse Devs` role. The value of this role during the testnet period is unknown.

Please do not modify this text as it will be used for the GitHub readme file.
