# Holidays on Hennepin 2026: decorating catalog

A static web page where Uptown businesses pick decorations and craft supplies for their $300 Holidays on Hennepin decorating grant. The committee buys and delivers everything; businesses never pay.

This site is for invited businesses and is not indexed by search engines.

## How it works
- `index.html`: the catalog. Reads `items.json`, `presets.json` and `businesses.json` (business names only, no contact details).
- `config.js`: budget, reply address, and the order-submission URL.
- `order.html`: view-only order summary, opened from the link in the confirmation email.
- Submitted orders go to a private Google Sheet through a Google Apps Script web app. No order data is stored in this repository.

## Privacy
No business or volunteer contact details belong in this repository. Contact name and email are typed by each business at order time and stored only in the private Sheet.

## Updating items
Item and set data live in `items.json` and `presets.json`. Edit those files (or ask the maintainer to re-import them from the committee's item spreadsheet) and push to `main`; GitHub Pages republishes automatically.

## Run locally
    python3 -m http.server 8765
Then open http://localhost:8765
