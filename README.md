# 🎂 Zamzam Bakes

A clean, single-page website for **Zamzam Bakes** — a home-based bakery in Mangalore, India. Built with pure HTML/CSS/JS, deployed on Vercel.

**Live:** [zamzambakes.vercel.app](https://zamzambakes.vercel.app)

---

## What It Does

- Showcases the bakery's menu (custom cakes, cupcakes, brownies, macarons, etc.)
- Lets customers place orders via a form that auto-generates a WhatsApp message
- Displays a gallery of real orders with hover overlays
- Shows location info (BC Road, Mangalore & Moodbidri) with an embedded Google Map
- Links to Instagram [@zamzam_bakes_](https://www.instagram.com/zamzam_bakes_/)

---

## Stack

| Layer      | Tech                        |
|------------|-----------------------------|
| Frontend   | HTML, CSS, Vanilla JS       |
| Fonts      | Google Fonts (Playfair Display + Inter) |
| Deployment | Vercel                      |
| Ordering   | WhatsApp deep link (`wa.me`) |

No frameworks, no build step, no dependencies.

---

## Project Structure

```
zamzam-bakes/
├── index.html          # Entire site (single file)
├── vercel.json         # Vercel SPA rewrite config
├── images/
│   ├── almond-cake.jpg
│   ├── choco-drip-cake.jpg
│   ├── pudding.jpg
│   ├── strawberry-cake.jpg
│   ├── wedding-cake.jpg
│   └── wedding-cake-nobg.png
└── .vercel/            # Vercel project config (auto-generated)
```

---

## Sections

1. **Hero** — tagline, badges, CTA buttons, featured image
2. **Stats** — 100% fresh ingredients, custom orders, 2 locations
3. **About** — story, highlights, photo grid
4. **Scrolling Ribbon** — animated menu of what's available
5. **Menu** — 6 cards with photos, descriptions, and pricing
6. **How It Works** — 4-step order process
7. **Order Form** → WhatsApp — collects name, phone, item, date, flavour, notes
8. **Gallery** — 5 real-order photos with hover overlays
9. **Location** — cards + embedded Google Map
10. **Instagram CTA** + **Footer**
11. **Floating WhatsApp button** — always visible

---

## Ordering Flow

1. Customer fills the form
2. On submit, a pre-filled WhatsApp message is generated and opened in a new tab
3. Customer sends the message → bakery confirms on WhatsApp

To change the WhatsApp number, update `waNumber` in the `<script>` block at the bottom of `index.html`:

```js
const waNumber = '919900701382'; // Replace with your number (country code + number, no +)
```

---

## Deploy

Already connected to Vercel. To redeploy:

```bash
# If using Vercel CLI
vercel --prod
```

Or just push to the connected Git branch — Vercel auto-deploys.

---

## Local Preview

No build needed. Just open `index.html` in a browser:

```bash
# macOS / Linux
open index.html

# Windows
start index.html
```

Or use VS Code's Live Server extension.

---

## Design Tokens (CSS Variables)

| Variable       | Value     | Used for                  |
|----------------|-----------|---------------------------|
| `--cream`      | `#FDF6EE` | Page background           |
| `--rose`       | `#C9847A` | Primary accent / buttons  |
| `--brown`      | `#3B1F0E` | Headings, nav             |
| `--gold`       | `#C8994A` | Ribbon accents            |
| `--text-muted` | `#7A5C46` | Body copy                 |
