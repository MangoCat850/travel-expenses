# Travel Expense Tracker

A shared, real-time travel expense tracker built as a single HTML page, hosted on GitHub Pages.

**Live URL:** https://mangocat850.github.io/travel-expenses/

---

## Features

- Add expenses with a title, date, category, amount, and who paid
- Three country tabs — 🇨🇦 Canada (CAD), 🇨🇳 China (YUAN), 🇯🇵 Japan (YEN)
- Currency is automatically assigned based on the active country tab
- Real-time sync via Firebase — both J and C see the same list instantly
- Interactive charts — category breakdown (doughnut) and daily spend by person (stacked bar)
- Filter expenses by category or payer
- Delete individual expenses or clear all

---

## How to Use

### Adding an Expense
1. Enter a **title** (e.g. "Ramen in Shinjuku")
2. Select a **date** — defaults to 2026, stays as last used after each save
3. Choose a **category**: Food, Commute, or Leisure
4. Enter the **amount**
5. Select who **paid**: J or C
6. Click **Add Expense**

The currency is set automatically by whichever country tab is active on the right panel.

### Country Tabs
| Tab | Currency |
|-----|----------|
| All | Shows all three tables |
| Canada | CAD |
| China | YUAN |
| Japan | YEN |

Switching tabs also updates the active currency for new expenses.

### Charts
- **By Category** — doughnut chart showing count of expenses per category across all entries
- **J vs C** — stacked bar chart showing total amount spent per day, broken down by J (blue) and C (purple). Respects the active country tab currency.

### Filters
Use the filter chips (All / Food / Commute / Leisure / J / C) to narrow down the expense tables within the active tab.

---

## Real-Time Sync

Expenses are stored in a Firebase Realtime Database. Any change made by J or C (add or delete) is reflected on the other person's screen instantly without refreshing.

A **Live** indicator (green dot) in the header confirms the connection is active. If offline, adding expenses is disabled until reconnected.

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Vanilla HTML, CSS, JavaScript |
| Charts | Chart.js via CDN |
| Database | Firebase Realtime Database |
| Hosting | GitHub Pages |

---

## Changelog

| Date | Update |
|------|--------|
| 2026-03-20 | Initial build — expense form, categories, currency, payer, localStorage |
| 2026-03-20 | Added date field with 2026 default year |
| 2026-03-20 | Replaced localStorage with Firebase Realtime Database for live shared sync |
| 2026-03-20 | Added Canada / China / Japan country tabs with per-currency tables and total rows |
| 2026-03-20 | Removed currency dropdown — currency now set by active country tab |
| 2026-03-20 | J vs C chart changed to stacked bar by date with total spend on y-axis |
| 2026-03-20 | Date field no longer resets after submitting — retains last used date |
| 2026-03-20 | Added travel.md documentation |
