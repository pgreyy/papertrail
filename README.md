# PAPERTRAIL

Readable books for stablecoin businesses. Built on Arc.

## The problem

Businesses settling in stablecoins end up with thousands of raw

transactions and no way to read them. No categories, no counterparty

names, no statement, nothing an accountant or a tax filing can use.

The payment rails are solved. The layer that makes spending legible

to the humans responsible for it does not exist.

This gets an order of magnitude worse with agent spending, where a

single agent can generate tens of thousands of sub-cent nanopayments

in a month.

## The solution

Point it at a wallet. Get back a statement you can actually read.

1. Ingest transaction activity from Arc

2. Classify each transaction by counterparty and purpose

3. Render a clean statement: money in, money out, by category,

   top counterparties, period-over-period change

4. Flag anomalies (a cost line that tripled since last period)

5. Export to CSV

## Built with

- **Arc Testnet** (chain ID 5042002) as the settlement layer

- **USDC** as the unit of account and gas

- **Circle Developer-Controlled Wallets** to provision the business

  wallet and counterparties

- **Arc Memo transaction extension** to carry structured context

  on-chain for classification

- **Circle Gateway / Nanopayments** for the agent-spend data path

## Stack

Next.js, Supabase, viem

## Status

Week 3 of 4. Scope locked, environment set up, ingestion in progress.

## Roadmap

Budgets and spend controls, approval flows, accounting software

export, agent-level cost attribution.
