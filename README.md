# Torn Market Scout

Find underpriced Item Market listings in Torn and keep an eye on what you hold. It runs entirely in your browser: there is no server, and your API key never leaves your device except to talk to Torn.

## What it does

- **Scans the Item Market** and flags two kinds of opportunity:
  - *Priced below value*: listings that sit under Torn's average price by more than the fee and your minimum margin.
  - *Gap flips*: the cheapest listing is far below the next one, so you can buy it and relist just under the second price.
- **Shows the math**: profit per item after the market fee, return on cost, and total profit within your cash budget.
- **Tracks price history** in your browser, and tells you when an item is cheap or expensive compared with its own usual price.
- **Watchlist** for items you hold or want to buy: set what you paid for sell alerts, or a buy-below price for buy alerts. Optional auto-refresh with a sound.

## Use it

1. Open the page.
2. In Torn, go to Settings, API Keys and create a key. A public-access key is enough.
3. Open Settings in the app, paste the key, and press **Load item list**.
4. Press **Scan next batch**. It checks the most valuable items first and respects Torn's rate limit.

Tune the fee, minimum profit, minimum return, cash budget and item filters under Settings. The market fee defaults to 5%. Change it if Torn's rate is different.

## Put it on GitHub Pages

1. Create a new repository on GitHub (public is fine, the page contains no secrets).
2. Upload `index.html` and this `README.md`.
3. Open the repository's **Settings**, then **Pages**.
4. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and the `/ (root)` folder, and save.
5. After a minute, your page is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`. Share that link.

To update later, upload a new `index.html` to the repository.

## Privacy and keys

- Each person enters their own API key. It is stored in that person's browser (`localStorage`) and sent only to `api.torn.com`.
- Nobody else, including whoever hosts the page, can see it.
- Settings has an **Erase saved data** button, useful on a shared computer.
- Never paste your key into a copy of this page you did not get from a source you trust.

## Limits worth knowing

- Estimates assume you can sell at the target price. Thin markets, price moves between scan and purchase, and other buyers can erase a margin.
- Torn allows roughly 100 API requests a minute per key, so a batch of 40 items takes about half a minute.
- Price history builds up over time: items need five or more of your own scans before the comparison to their usual price appears.

This is an unofficial tool and is not affiliated with Torn.
