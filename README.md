# Sushiswap-forked

# Quickstart

## Installation

```
npm install
```

## Run tests

```
npm test
```

## Configuration

Create a `.env` file with keys

```
MNEMONIC="..."
INFURA_ID="..."
ETHERSCAN_API_KEY="..."
```

* Deployment to rinkeby is done via [Infura](https://infura.io/).
* Create an [Etherscan API key](https://etherscan.io/myapikey) for contract verification.

_Forks of this project should also modify `config.json`. Decimals aren't considered in the configuration._

## Deployment

### Ganache

[Ganache](https://www.trufflesuite.com/ganache) is a personal Ethereum blockchain for development and
tests.

```
truffle migrate -- --network development
```

### Rinkeby

To deploy on the [Rinkeby](https://rinkeby.io/) Ethereum testnet, make sure your wallet has enough ETH to pay for the
GAS.

[Faucet 1](https://testnet.help/en/ethfaucet/rinkeby) | [Faucet 2](https://faucet.rinkeby.io/)

```
truffle migrate -- --network rinkeby
truffle run verify -- --network rinkeby
```

You may also want to verify the ERC20Mock and LPMock contracts on Etherscan.

```
node_modules/.bin/truffle verify ERC20Mock
node_modules/.bin/truffle verify LPMock
```

_Verification may fail because of rate limits. Just try again._

### Ethereum mainnet

```
truffle migrate -- --network mainnet
truffle run verify -- --network mainnet
```

## Deployed on Binance Smart Chain testnet 

SushiToken - https://testnet.bscscan.com/token/0xfe0b1a1683d12297d3e9cee3157e1aad355dc5d9 <br>
MasterChef - https://testnet.bscscan.com/address/0x695dD3EACB93679AA95b69fcf4D4f7F71cD31617#contracts <br>
(Uni|Sushi)UniswapV2Factory - https://testnet.bscscan.com/address/0x7B15AC23F3bE0baF59764e0c729c64D2623D78eF#code <br>
(Uni|Sushi)UniswapV2Router02 - https://testnet.bscscan.com/address/0x32398b255eFCD113a3640f2Df750a7749f83D222#contracts <br>
SushiBar - https://testnet.bscscan.com/address/0xA3745DA90211b4C776dd0fBA6F8AA2e26c966889#writeContract <br>
SushiMaker - https://testnet.bscscan.com/address/0x3dce5E4Ee0ffF4Ae7193c7d3F5277307b4460456#code <br>
Migrator - https://testnet.bscscan.com/address/0x2B2Df750AB5e8c51B4499e26C0EDA2CadECD8b7B#code
