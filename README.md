# Tally — payment requests for made-to-order sellers

A mobile-first prototype for Instagram sellers in Nigeria who take orders in DMs and get paid by bank transfer. Instead of invoices, Tally is built around the **order**: one customer, a deposit now and the balance later. From each order it makes a payment request, tracks what's still owed, sends WhatsApp reminders, and issues a receipt.

Built as a UX portfolio case study. There is no backend: all data stays in the browser (`localStorage`), and the app opens with a demo shop, Mimi Crochets.

## What's in it

- Onboarding, then a two-step shop setup (business name, bank details)
- Dashboard: money owed, the overdue share, earnings this month, overdue orders first
- Create a payment request: items, delivery, discount, deposit (none / 50% / custom), deadline
- A payment request and receipt that customers see, shared via a WhatsApp link with the amount and account number as plain text
- Record payments, track deposit → balance → paid, mark delivered
- Reminders in a friendly, neutral or firm tone. The seller always presses send.
- Customers with what they've spent and what they owe

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The app source: one file, React with JSX compiled in the browser. Edit this. |
| `dist/index.html` | The deployable build: the same app with JSX compiled ahead of time. |
| `serve.mjs` | A tiny local preview server with no dependencies. |
| `index-v*.html` | Earlier visual directions, kept as design history. |

## Run it locally

```bash
node serve.mjs
# open http://localhost:4173
```

## Deploy

`vercel.json` points Vercel at `dist/`, so importing this repo into Vercel needs no build settings.
