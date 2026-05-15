# SoFi Wheel Dashboard

Personal dashboard for tracking a cash-secured-put / covered-call ("wheel") strategy on SOFI.

**Live:** https://tdander26.github.io/sofi-wheel-dashboard/

The key question this answers at a glance: **are the premiums I'm collecting offsetting my unrealized loss on the shares?**

## What it does

- Manual trade entry with all the fields a wheel trader cares about (date, type, strike, expiration, premium, contracts, status)
- CSV import that auto-detects common brokerage column names
- CSV export for backup
- Position tracking: shares held, premium-adjusted cost basis, break-even price
- Premium tracking: total, puts vs calls, monthly chart, cumulative chart
- The headline metric: net position = premiums collected + unrealized P&L on shares, with a clear green/red indicator

## How to use

- Enter trades through the **+ New Trade** form, or import a CSV from your broker
- Type the current SOFI price in the price card to update unrealized P&L
- Click **Export CSV** periodically as a backup — data lives in `localStorage`
- Sample data loads on first visit; click **Clear sample data** when you're ready to enter real trades

## Notes

This is a tracking tool, not a trading tool. No live broker integration. All data is stored locally in your browser.

Built as a single HTML file (Chart.js via CDN) and hosted on GitHub Pages.
