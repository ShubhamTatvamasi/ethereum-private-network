# ethereum-private-network

Install Ethereum
```bash
brew install ethereum
```

Run `puppeth` for setting up private chain at `~/.puppeth/`
```bash
puppeth
```

Main account: 0x061b95F4eb54e4826f2012b25f583cc3ee112EFE

1. Please specify a network name: mychain
1. Configure new genesis
1. Create new genesis from scratch
1. Clique - proof-of-authority
1. seconds = 1
1. Which accounts are allowed to seal?: 0x061b95F4eb54e4826f2012b25f583cc3ee112EFE
1. Which accounts should be pre-funded?: 0x061b95F4eb54e4826f2012b25f583cc3ee112EFE
1. Should the precompile-addresses (0x1 .. 0xff) be pre-funded with 1 wei? (advisable yes): no
1. Specify your chain/network ID if you want an explicit one (default = random): 59568
1. Manage existing genesis
1. Export genesis configuration
1. Which folder to save the genesis specs into? (default = current): genesis.json

Start the blockchain
```bash
docker-compose run -d ethereum
```

Geth console
```bash
docker exec -it <container-name> geth attach
```
---

### Geth commands

Get the latest block number
```
eth.blockNumber
```

Get your account address
```
eth.coinbase
```

Get balance of your account
```
eth.getBalance(eth.coinbase)
```
