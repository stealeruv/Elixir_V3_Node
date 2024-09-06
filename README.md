# Elixir_V3_Node
Running an Elixir Testnet Validator

## Project Introduction

Introducing the next generation of orderbook liquidity: a modular network natively powering exchanges

Elixir is a modular DPoS network built to power liquidity on orderbook exchanges. 

​Elixir is cross-chain and composable: enabling orderbook DEXs to natively integrate Elixir Protoco - a decentralized protocol - into their core infrastructure to unlock retail liquidity for pairs, among other exciting use cases. The decentralized network serves as crucial underlying infrastructure allowing for exchanges and protocols to easily bootstrap liquidity to their books.

​Elixir has 30+ native integrations into the core infrastructure of leading DEXs

## Join our community for Airdrops & Nodes

**Youtube** : https://www.youtube.com/@cryptoconsole

**Follow X** : https://x.com/cryptoconsol

**Join TG** : https://t.me/cryptoconsol


### Requirements

| **Requirement**              | **Description**                     |
|------------------------------|-------------------------------------|
| Operating System             | Ubuntu 22.04 or newer               |
| Memory (RAM)                 | Minimum 8 GB                        |
| Disk Space                   | Minimum 100 GB of free disk space   |
| Bandwidth                    | 100Mbit/s                           |

### Install Dependencies

```
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git jq lz4 build-essential unzip
```
### Install Docker
Ignore if you already Installed

```
sudo apt install -y ca-certificates curl gnupg lsb-release
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io
sudo usermod -aG docker $USER
newgrp docker
```
### Make a Directory for Elixir
```
mkdir elixir && cd elixir
wget https://files.elixir.finance/validator.env
```
### Install Nano
Ignore if already installed

```
sudo apt install nano
```
### Edit .env file

```
nano validator.env
```

Create a new and dedicated wallet using metamask. Don't use old wallet.

STRATEGY_EXECUTOR_DISPLAY_NAME :Enter name for your Node

STRATEGY_EXECUTOR_BENEFICIARY : Enter the wallet address here

SIGNER_PRIVATE_KEY : Private key from the new wallet


Ctrl+X - they press Y - Enter

### Faucet

Get sepolia Eth from faucet or send it from another wallet.

Faucet link : https://www.alchemy.com/faucets/ethereum-sepolia

You need to have 0.001 Eth on mainnet.

### Docker pull

```
docker pull elixirprotocol/validator:v3 --platform linux/amd64
```

### Start the Node

```
docker run --env-file /root/elixir/validator.env --platform linux/amd64 -p 17690
```

### Mint Mock

- Visit Testnet staking : https://testnet-3.elixir.xyz/ ( you can use any wallet for this purpose)
- Mint mock tokens 
- Click on Custom validator
- Search for the node wallet address
- Stake the mock tokens on your validator.

## Join our TG for More updates on Elixir : https://t.me/cryptoconsolchat
