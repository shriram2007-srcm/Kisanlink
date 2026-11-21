# KisanLink: Farmer-to-Market Price & Sell Advice

KisanLink helps small farmers decide **when and where to sell their crops**. It compares nearby markets, shows the real take-home price after transport, forecasts the next 3 days, and gives one clear instruction in English, Tamil or Hindi.

Built for **INNOVATE INDIA Hackathon 2026, Round 2: Project Development**.

**Live demo:** https://shriram2007-srcm.github.io/kisanlink

## The problem

Small farmers often sell at low prices because they do not know current mandi rates or which nearby market has demand. Middlemen profit from this information gap, and farmers lose income or waste crops waiting for the right buyer.

## What the prototype does

- **Sell advice:** shows "Sell now at *market*" or "Hold 2-3 days, then sell at *market*", based on a 3-day price trend.
- **Market comparison:** ranks 5 nearby markets by take-home price (market price minus transport cost).
- **Price trend chart:** last 7 days of prices plus a 3-day forecast.
- **Price alert:** set a target price and get a banner when any market reaches it.
- **Three languages:** English, Tamil (தமிழ்) and Hindi (हिन्दी).
- **Voice support:** "Read aloud" speaks the advice in the selected language.
- **Direct buyers:** a list of buyers with call buttons, to reduce dependence on middlemen.
- **Refresh prices:** simulates a market update so you can see advice and alerts change live.

Supported crops: tomato, onion, banana, groundnut and paddy.

## How the advice is calculated

1. For each market, take-home price = market price - (distance in km x ₹2.5 per quintal per km).
2. The market with the highest take-home price is the best market.
3. A linear regression on that market's last 7 daily prices forecasts the next 3 days.
4. If the forecast rises by more than 2 percent, the advice is to hold; otherwise, sell now.

## Tech stack

**Prototype**
- HTML5, CSS3 and vanilla JavaScript (single file, no build step)
- SVG for the trend chart
- Web Speech API for voice output
- Google Fonts (Mukta) for Tamil, Hindi and English text

**Planned for the full version**
- Government Agmarknet open data API for live mandi prices
- Python (FastAPI) backend
- Firebase or MongoDB database
- Flutter mobile app
- Trained price prediction model

## Run it locally

No installation needed.

```bash
git clone https://github.com/YOUR-USERNAME/kisanlink.git
cd kisanlink
```

Then open `index.html` in any modern browser.

## Important note on data

This prototype uses **sample market data** generated in the browser, so prices are illustrative and not real. Buyer names and phone numbers are placeholders. The full version will fetch live prices from Agmarknet through a backend.

## Roadmap

- Connect live Agmarknet data through a FastAPI backend
- Train a proper price forecasting model on historical data
- SMS and WhatsApp alerts for low-connectivity areas
- More crops, markets and states
- Weather and transport cost insights
- Verified buyer listings

## Impact

- Farmers earn more by selling at the right time and place
- Less dependence on middlemen
- Reduced crop wastage
- Supports Digital India and rural income growth

## Author

**YOUR FULL NAME**
INNOVATE INDIA Hackathon 2026 (individual participation)
