# SUN Token

SUN is a fixed-supply TRC20 token on the TRON network. This repository contains the token contracts and their TronBox build configuration.

## Token details

| Property | Value |
| --- | --- |
| Name | SUN TOKEN |
| Symbol | SUN |
| Network | TRON |
| Standard | TRC20 |
| Decimals | 18 |
| Total supply | 19,900,730,000 SUN |

The full supply is minted once during deployment to the nonzero address passed to `SunToken(address gr)`. The contract supports transfers, approvals, delegated transfers, and allowance adjustments through `increaseAllowance` and `decreaseAllowance`. Balance and allowance arithmetic uses SafeMath.

## Contract addresses

| Network | Contract |
| --- | --- |
| Mainnet | [`TSSMHYeV2uE9qYH95DqyoCuNCzEL1NvU3S`](https://tronscan.org/contract/TSSMHYeV2uE9qYH95DqyoCuNCzEL1NvU3S) |
| Nile testnet | [`TDqjTkZ63yHB19w2n7vPm2qAkLHwn9fKKk`](https://nile.tronscan.org/contract/TDqjTkZ63yHB19w2n7vPm2qAkLHwn9fKKk) |

## Build

Requires Node.js 22 or 24.

```sh
npm ci --ignore-scripts
npm run compile
```

The project uses TRON Solidity 0.5.8 with optimization enabled and 200 runs. TronBox downloads the compiler on the first build and writes compiled artifacts to `build/contracts/`.

## Project structure

```text
contracts/
  SunToken.sol      Token constructor and initial supply
  BaseTRC20.sol     Transfers, allowances, and token metadata
  ITRC20.sol        TRC20 interface and events
  Context.sol       Caller context
  SafeMath.sol      Checked arithmetic
tronbox-config.js   Compiler configuration
```
