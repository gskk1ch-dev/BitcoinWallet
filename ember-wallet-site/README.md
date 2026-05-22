# Ember Wallet — Live Demo

An educational, multi-asset crypto wallet interface (Ledger-inspired), built for the
university project *"Modern technologies and crypto wallets for daily use."*

**Live site:** once GitHub Pages is enabled, this runs at
`https://<your-username>.github.io/<repo-name>/`

> ⚠️ Educational demo only. No real cryptography, no real funds. All balances, prices,
> addresses, seed phrases, and transactions are simulated. The only live network calls are
> the public Bitcoin market price and the public wallet-data link.

## What it does

- Multi-asset portfolio with live-ticking prices and a privacy toggle
- Send / Receive with QR codes (simulated, balances update locally)
- Transaction history
- Restore from a recovery phrase or private key, with a decrypt/sync sequence and
  password-creation step
- After a private-key restore, shows Bitcoin with a **real, live market price**
- Reads its wallet name, balances, transaction history, and all interface text from a
  public data file (a GitHub Gist), so the content is editable without changing code

## Files

- `index.html` — the entire app, self-contained (React + Babel bundled inside)
- `wallet-data.txt` — a reference copy of the data format (the live app fetches its data
  from a public GitHub Gist configured inside the app, editable under Settings)

## How it's hosted

This is a static site: a single `index.html`. GitHub Pages serves it directly — no build
step, no server. Because it's served over HTTPS, the app can fetch the public Bitcoin price
and the Gist-hosted wallet data.
