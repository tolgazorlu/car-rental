# Car Rental Platform

A Solidity smart contract for a peer-to-peer car rental marketplace on BNB Smart Chain.

## About

`CarRentalPlatform` lets an owner list cars for rent or sale, and lets users register, rent a car, pay rent, and settle debt, with balances tracked on-chain. Built June 2023 as a Truffle/BNB Smart Chain project.

## Features

- Add, edit, and retire car listings (name, image URL, rent fee, sale fee, status)
- User registration with on-chain profile (name, last name, wallet)
- Rent a car and track rental start time, accrued debt, and balance
- Reentrancy protection via OpenZeppelin's `ReentrancyGuard`
- Truffle test suite covering user and car creation flows

## Tech stack

- Solidity ^0.8.7
- Truffle (compile, migrate, test)
- OpenZeppelin Contracts (`Counters`, `ReentrancyGuard`)
- BNB Smart Chain (via `@truffle/hdwallet-provider`)

## Project structure

```
contracts/bsc/CarRentalPlatform.sol   # main contract
migrations/                           # Truffle migration scripts
test/carRentalPlatform.js             # Truffle test suite
truffle-config.js / truffle-config.bsc.js
```

## Getting started

```bash
npm install
npm run compile      # truffle compile
npm test             # truffle test
npm run migrate:bsc --network <network>   # deploy to BNB Smart Chain
```

Create a `.env` file with a `MNEMONIC` value for the network you deploy to (see `truffle-config.bsc.js`).

## Status

Learning/experiment project, not actively maintained.

## License

MIT, see `LICENSE`.
