# THE EL — Volatility Terminal

A single-file trading terminal for [Deriv](https://deriv.com) synthetic volatility indices.
No build step, no dependencies: `index.html` is the whole app.

## Features
- **Trade** — live tick chart, digit-aware quote, over/under/even/odd/matches/differs/rise/fall tickets, live payout quotes, open contracts with one-click sell, recent trade history.
- **Signals** — six digit setups scored on hit rate, streak and "dry" gaps, with per-card thresholds, plus a one-click scan across every volatility index.
- **Analysis** — digit distribution against the 10% baseline, hot/cold heatmap, last-digit strip, and over/under probability per barrier.
- **Bots** — five presets (streak, streak fade, cold digit, even/odd imbalance, martingale) with take-profit, stop-loss, max consecutive losses and cooldown gates.

## Use it
1. Open the deployment URL.
2. Log in with Deriv (OAuth). Demo account by default — real accounts show a confirmation before any bot runs.
3. Trading needs your own App ID: register at [api.deriv.com](https://api.deriv.com), add this page's URL as the redirect URL, then paste the App ID in **⚙ Settings**. Until then the page streams public market data read-only.

App ID and preferences live in `localStorage`; the session token lives in `sessionStorage` and is never sent anywhere except Deriv's own WebSocket.

## Deploy
Static file — host anywhere (Vercel, Netlify, GitHub Pages, S3). Nothing to build.

> Risk notice: digit and rise/fall contracts are high-risk products. Signals and bots here are informational tools, not advice.
