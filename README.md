# SBR – Shady Business Rating

**Free 0–100 risk rating for any Solana wallet, token or NFT, built only from on-chain evidence.**

Live: **https://shadybusinessrating.com** (also at https://rumplebitskin.com/sbr/)

0 = legit · 100 = shady · 0–30 LEGIT · 31–70 CAUTION · 71–100 SHADY

---

## What it checks

**Wallets** – age, .sol name, organic use, failed-transaction rate, bot patterns, pass-through / fee drains,
dust and airdrop spam, tokens launched and how they went (dumps, bundles, insiders, pulled liquidity, self-trading),
drainer sweeps (wallets that receive a fixed-split share of emptied wallets), funder profile, bridges.
Also: a free **"Was I drained?"** check, a **"Where did it go?"** money trace, a PDF report, and a token-approval
checker with one-click revoke.

**Tokens** – mint/freeze authority, Token-2022 extensions (permanent delegate, hooks, fees), the creator found from the
launch transaction (or pump.fun bonding curve), whether the creator sold at launch, insider and bundled holdings,
top-10 concentration, liquidity pulled, Rugcheck flags, and the creator wallet's own SBR.

**NFTs** (standard, programmable, Metaplex Core and compressed) – link / airdrop bait (the drainer lure), verified
collection and creator, who can still move, freeze or change it, where the art lives, wash-like trading,
**whether the team sold during the mint**, and the creator's own SBR. Wallet scans list the wallet's NFTs and flag bait.

## How the score works

Score = 100 × sigmoid(prior −1 + the sum of every factor's log-odds). Every factor shows its measured value and how
much it moved the dial, so nothing is hidden. Each scan is pinned to a finalized Solana slot:
**same address + same snapshot = same reading.** The full factor list, weights and changelog are on the page under
**"How SBR works"**.

## Free, and nobody can pay for a better score

SBR is free. No account, no sign-up, no payments. On the public site you get a daily number of new-address scans,
then one new address every 30 seconds; rescans of an address within 24 hours are always free. You can also add your own
Helius API key in Settings for unlimited scans – the key stays in your browser.

SBR is an automated rating of public on-chain behavior. It is **not financial advice and not an accusation.**
Owners can post a signed note on their own address from inside SBR.

## What's in this repo

| File | What it is |
|---|---|
| `index.html` | The complete SBR page (one file: HTML, CSS and JavaScript). This is exactly what runs on the live site. |
| `README.md` | This file. |

No API keys or secrets are in this code. On the public site, scans go through a small server that holds the site's own
Helius key; with your own key, the page talks to Helius directly from your browser.

**Run it yourself:** download `index.html`, open it in a browser, add a Helius API key (free at
https://dashboard.helius.dev) in Settings, and scan.

## Data sources

Helius RPC, Enhanced Transactions and DAS · Bonfida SNS · Rugcheck · Jupiter and DexScreener (market info, shown for
context, never scored).

## Contact

- X: [@rumplebitskin](https://x.com/rumplebitskin)
- Email: contact@rumplebitskin.com
- Home: https://rumplebitskin.com

Built by **rumplebitskin.sol** – a one-man project.
