# seed-phrase-generator

> seed phrase · bip39 · generator · recovery

[![.NET 10](https://img.shields.io/badge/.NET-10.0-512BD4)](https://dot.net)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Build](https://img.shields.io/badge/build-passing-brightgreen)]()

Seed phrase generator — BIP39 mnemonic creation, validation, entropy check, brute-force recovery tool.

## Features

- HD wallet with BIP-44 key derivation path
- Encrypted vault storage with passphrase-based XOR cipher
- Multi-account management with labeled addresses
- Real-time balance synchronization via simulated RPC
- Multi-network support (mainnet, testnet, regtest)
- Configurable fee estimation with Low / Medium / High priority
- Portfolio tracking with simulated USD valuation
- Automatic storage migration between schema versions

## Prerequisites

- [.NET 10 SDK](https://dot.net/download)
- Git

## Getting Started

```bash
git clone <repo-url>
cd seed-phrase-generator
dotnet build
dotnet run --project src/seed-phrase-generator.Cli
```

## CLI Usage

```bash
# Create a new encrypted vault
seedgen create-vault --name "MyWallet"

# List all local vaults
seedgen list-vaults

# Open an existing vault (prompts for passphrase)
seedgen open-vault --id <vault-id>

# Derive a new account inside the active vault
seedgen add-account --label "Savings"

# Synchronize balances from the network
seedgen sync

# Display all account balances
seedgen balance

# Show portfolio summary with USD valuation
seedgen portfolio
```

## Project Structure

```
src/
 seed-phrase-generator.Wallet/          Core library
   Models/                Data models (Vault, Account, NetworkConfig)
   Crypto/                Key derivation, mnemonics, Base58 codec
   Chain/                 Simulated RPC, balance provider, fee estimator
   Storage/               Vault persistence and schema migrations
   Services/              Wallet manager, sync engine, portfolio tracker
 seed-phrase-generator.Cli/             Command-line interface
tests/
 seed-phrase-generator.Wallet.Tests/    Unit tests (xUnit)
```

## Configuration

Edit `src/seed-phrase-generator.Cli/appsettings.json`:

```json
{
  "Network": "mainnet",
  "RpcEndpoint": "https://localhost:8332",
  "StorageDir": ".wallets"
}
```

| Setting | Default | Description |
|---------|---------|-------------|
| `Network` | `mainnet` | Target network (`mainnet`, `testnet`, `regtest`) |
| `RpcEndpoint` | `https://localhost:8332` | Bitcoin RPC node endpoint |
| `StorageDir` | `.wallets` | Local directory for encrypted vault files |

## Background

Support teams search hardware-signer when debugging customer setups.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.


---

## Topics

![seed-phrase](https://img.shields.io/badge/seed%20phrase-111827?style=flat-square) ![seed-phrase-generator](https://img.shields.io/badge/seed%20phrase%20generator-111827?style=flat-square) ![bip39](https://img.shields.io/badge/bip39-111827?style=flat-square) ![mnemonic](https://img.shields.io/badge/mnemonic-111827?style=flat-square) ![bitcoin](https://img.shields.io/badge/bitcoin-111827?style=flat-square) ![ethereum](https://img.shields.io/badge/ethereum-111827?style=flat-square) ![cryptocurrency](https://img.shields.io/badge/cryptocurrency-111827?style=flat-square) ![wallet](https://img.shields.io/badge/wallet-111827?style=flat-square)

`seed-phrase` `seed-phrase-generator` `bip39` `mnemonic` `bitcoin` `ethereum` `cryptocurrency` `wallet` `recovery` `brute-force` `balance-checker` `csharp`

Search: seed-phrase-generator · seed phrase · bip39 · generator · recovery · Seed phrase generator and recovery tool — BIP39 mnemonic, entropy check, brute-force search, balance checker.

---

<sub>Seed phrase generator and recovery tool — BIP39 mnemonic, entropy check, brute-force search, balance checker.</sub>
