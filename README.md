# Personal Finance Tracker

A single-file, client-side personal finance tracker. No backend, no accounts, no dependencies to install — just open [`index.html`](./index.html) in a browser. All data is stored locally in the browser's `localStorage`.

## Features

- **Dashboard** — net worth, monthly income/expenses, savings rate, spending
  donut, income-vs-expense bars, upcoming bills, recent transactions
- **Transactions** — add/edit/delete with filters (type, category, account,
  month, text search) and a running net total
- **Budgets** — per-category monthly budgets with progress bars that shift
  green → yellow → red as you approach the limit
- **Recurring bills** — weekly, biweekly, monthly, quarterly, yearly; a "Pay"
  button records the transaction and advances the next-due date
- **Accounts** — checking, savings, credit, investment, cash, loan, other;
  credit-card balances correctly reduce net worth
- **Analytics** — 12-month cash flow, per-category trend, top spending
  categories for the year, monthly savings rate
- **Import / Export** — JSON round-trip of the full dataset
- **Net-worth history** — snapshotted once per day, charted over time

## Usage

1. Download or clone the repo.
2. Open `index.html` in any modern browser (double-click the file).
3. Start adding accounts, categories, transactions, and bills.

Data lives under the `localStorage` key `financeTracker.v1` in whichever browser
you open the file in. Use the **Export** button to back up your data as JSON and
**Import** to restore it elsewhere.

Chart.js is loaded from a CDN, so the first load needs internet access; after
that the app works offline.

## Tech

- HTML + vanilla JavaScript, one file
- [Chart.js](https://www.chartjs.org/) for the charts
- Browser `localStorage` for persistence
