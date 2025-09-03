## 🧩 Guide on Irys Storage CLI Node Using ETH sepolia as token :

Irys CLI is a tool to interact with a decentralized data layer, letting you upload, manage and access files or metadata on chain or off chain with permanent storage

---

## Requirements
### Hardware

* Memory - minimum 4GB
* Disk -  minimum 10-20GB SSD

### Software
* Supports: Ubuntu 20.04/22.04/24.04

* use burner wallet
* use ETH sepolia RPC from : [Chainlist](https://chainlist.org/)
* Get ETH sepolia Faucet: [Sepolia Mining](https://sepolia-faucet.pk910.de/)
  
## Install dependecies :

```
sudo apt-get update && sudo apt-get upgrade -y
```

```
sudo apt install curl iptables build-essential git wget lz4 jq make protobuf-compiler cmake gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev screen ufw -y
```


## Install nodejs & npm :

```
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && sudo apt install -y nodejs
```

### Check version :

```
node -v
npm -v
```

---

## Install CLI :

```
sudo npm i -g @irys/cli
```

### Verify installation :

```
irys 
```

---

## Parameters & Their Usage

| Option         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `-n`           | The network to check, `mainnet` or `devnet`, defaults to `mainnet`.         |
| `-t`           | The [token](https://docs.irys.xyz/build/d/features/supported-tokens) to use when funding.                                              |
| `-w`           | Your private key. (without 0x)                                                           |
| `--tags`       | Tags to include, format `<file_name> <file_format>`.                                   |
| `--provider-url` | RPC URL to use.   [FROM_HERE](https://chainlist.org/)                                                        |

---

* Now deposit testnet tokens

```
irys fund 1000000 \
  -n devnet \
  -t ethereum \
  -w Private_Key \
  --provider-url RPC_URL
```

* The fund amount is in `wei`
* Replace `Private_key` with your actual key (without 0x)
* Replace `RPC_URL` with your selected network - as said above

---


## Check Balance 

```
irys balance WALLET_ADDRESS \
  -t ethereum \
  -n devnet \
  --provider-url RPC_URL
```
* Replace `WALLET_ADDRESS` with your actual address : and `RPC_URL` also

---

## Upload a File :

* visit `this pc` in your laptop/pc > ubuntu > root folder > paste any img/video (not personal stuff)

* **visit ubuntu : paste `ls -a` to verify the file**

### Now paste :

```
irys upload FILE_NAME \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --tags FILE_NAME FILE_FORMAT \
  --provider-url RPC_URL
```

* change `FILE_NAME` to actual file
* change `PRIVATE_KEY` to real key (without 0x) - use burner wallet
* change `FILE_NAME` and `FILE_FORMAT` (PNG,JPG,MP4,MKV)
* change `RPC_URL` to your RPC

---
* done
