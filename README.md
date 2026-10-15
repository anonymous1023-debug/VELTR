# VELTR — Market Learning Playground

## Run it
- Open `index.html` in a current desktop/mobile browser.
- For best compatibility with public crypto quote requests, run a local server:
  - Python: `python -m http.server 8000`
  - Then open `http://localhost:8000`
- No install or API key is required for the simulator.

## Features
- Responsive liquid-glass style UI, dark/light theme.
- Simulated price ticks for sample stock, ETF, forex and commodity instruments.
- Sample 1D–5Y chart history, SMA, EMA, Bollinger overlays, volume bars, crosshair interaction.
- Demo market buy/sell orders, cash balance, holdings, P&L and order history.
- Monthly ₹10,00,000 virtual-cash credit, checked when the app is open. State is stored in local browser storage.
- Instrument directory, market filters, watchlist, screener, alerts, position calculator and trade journal.
- Best-effort public CoinGecko quote request for a small crypto subset. API/CORS/rate limits can prevent this; the app falls back to simulated prices.

## Important limitations
This is a front-end learning prototype, not a production trading platform. Most quotes and all long-range chart histories are synthetic and are clearly labelled as simulated. Crypto public quotes are best-effort and not guaranteed live or complete. There is no broker, exchange execution, licensed market-data feed, authentication, cloud sync, taxes/fees/slippage model, or exhaustive worldwide symbol database. Do not use demo data to make investment decisions.

## To make it genuinely live
Choose a licensed market-data provider for each required exchange/asset class, review its redistribution terms, and add a backend that protects API credentials, normalizes symbols, streams updates over WebSocket, and persists users/trades securely. A browser-only static page cannot safely contain private API keys.

## Windows quick start
Double-click `start.bat` if Python is installed. It starts a local web server and opens `http://localhost:8000`. Otherwise, open `index.html` in Chrome; simulation features still work, while the optional public crypto request may be blocked by browser file-origin restrictions.


## Trading styles, F&O, and local profile (prototype)
- Trade-style selector includes scalping, intraday, swing, short-term, positional, long-term, and delivery. The selected style is recorded with each simulated fill; this is a learning UI, not an execution engine.
- Separate F&O desk shows sample futures contracts and calls/puts in a sample options chain. Contracts, expiries, strikes, prices and lot sizes are illustrative and not verified exchange instruments. Margin, Greeks, settlement and expiry rules are not implemented.
- Login/sign-up is a local demo profile (display name and email saved in this browser only). There is no server-side authentication, password storage, account recovery, or cross-device sync. Do not enter sensitive data.
