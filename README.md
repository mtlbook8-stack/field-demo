# Field App Demo

A single-file, mobile-first clickable HTML demo of the Field App used by sales people and drivers at a beverage wholesale distributor. Mirrors the WholesaleERP PWA, plus four additive features: driver experience, notifications, tasks, and payment links.

## Run

```bash
python -m http.server 5173
```

Then open <http://localhost:5173> in a phone-sized browser pane (390 × 844). On desktop it renders inside a phone frame; on mobile it goes fullscreen.

## What's inside

- **Single `index.html`** — vanilla JS, Tailwind via CDN, Lucide icons, no build step.
- All data is inline mock data; state lives in memory only and resets on refresh.
- Hash-based router: `#home`, `#customers`, `#customers/:id`, `#orders`, `#orders/:id`, `#orders/new`, `#payments`, `#returns`, `#returns/new`, `#reports`, `#settings`, `#notifications`, `#tasks`, `#payment_links`, `#route`, `#stops/:id`.

## Highlights

- 4-step Order Wizard (Select Customer · Build Order · Review Order · Confirmation) with catalog/favorites/top modes, discount caps, deposit sub-lines, credit/prepay checks.
- 7-tab Customer Profile with branch/parent billing, saved payment methods, notes.
- 3-step Returns wizard with damage marking, line splitting, and reason selection.
- Payment collection with a 5-method modal (Cash/Check/Card/ACH/Account Credit) and Send Payment Link.
- Reports hub, Notifications center, Tasks, and Payment Links — all functional in memory.
- Driver role (toggle in Settings): Route + Stop Detail with a signature canvas and refuse reasons.

Switch between **Sales Person** and **Driver** roles in Settings to change the leftmost nav tab between Home and Route.
