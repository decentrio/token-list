# Soroban Indexer

A config to manage and query liquidity pools, tokens, and tickers on the Soroban network.

## Features

- **Liquidity Pools**: track pool addresses, staking contracts, and share tokens.
- **Tokens**: view and manage details for supported tokens, including their Soroban contract IDs and decimals.
- **Tickers**: currency pairs and associated pool contracts.

## Data Files

- `pool_lists.json`: contains details of liquidity pools with addresses, staking contracts, and share tokens.
- `token_lists.json`: lists supported tokens with symbols, Soroban contract IDs, and decimals.
- `ticker_lists.json`: includes ticker information for currency pairs and their associated pool contracts.

## Usage

1. Get the details
   ```bash
   soroban contract invoke \
   --rpc-url "https://mainnet.sorobanrpc.com" \ # can be any public one
   --network-passphrase "Public Global Stellar Network ; September 2015" \ # should be always this one (can change)
   --source <YOUR-PUBLIC-ADDRESS> \
   --id "CB4SVAWJA6TSRNOJZ7W2AWFW46D5VR4ZMFZKDIKXEINZCZEGZCJZCKMI" \ # address of the factory contract
   -- \
   query_pool_details \
   --pool_address <ADDRESS-OF-POOL-TO-QUERY> | jq
   ```
