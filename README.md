# Frontend-Demo-for-Business-Website
Single-file installable PWA for RK Jewellery: profit margin calculator, Marathi social media caption generator, A4 purchase order / invoice, and PDF, Excel and Word export.

# 💎 RK Jewellery Business Suite

A single-file, installable Progressive Web App (PWA) for **RK Jewellery**, Shirpur, Maharashtra. It combines pricing, social media captions and invoicing in one dark-and-gold dashboard that runs in the browser or as a Windows desktop app. There is no backend and no build step.

Built with HTML5, Tailwind CSS, Font Awesome 6 and vanilla JavaScript.

## Features

### Smart pricing and margin engine
- Cost price input with quick margin chips (15%, 20%, 30%, 50%, 100%) and a custom % box
- Live KPI cards for selling price, gross profit and net profit
- Net profit is worked out after shipping (₹80), packaging (₹40) and an optional 3% GST buffer
- A deductions breakdown shows the in-hand net profit

### Occasion and campaign switcher
- **Normal**: standard daily retail pricing and the classic Marathi caption
- **Diwali special offer**: festive greeting, 🪔 emojis and a discount %
- **Occasion off**: plain price line with no promotional wording
- **Custom offer**: type any festival or event (Gudi Padwa, Akshaya Tritiya, Wedding Season and so on)
- The chosen occasion updates the caption, the invoice banner and the discount row

### Marathi caption generator
- Fills in the final selling price automatically
- Changes the shipping line based on the delivery state
- Editable textarea with one-click copy and direct WhatsApp sharing

### Delivery logic
- Maharashtra: ₹0 shipping with a **Free Shipping** badge
- Other states: flat ₹100 shipping added to the invoice and the caption

### Purchase order / tax invoice
- A4-style invoice with gold branding
- Editable seller and buyer details, with a state dropdown
- Multi-item table with add and remove rows
- Subtotal, festive discount, manual discount, shipping, optional 3% GST and grand total
- Authorized signatory box and terms and conditions

### Export station
| Format | Library |
|---|---|
| PDF (A4) | html2pdf.js, plus browser Print |
| Excel (.xlsx) | SheetJS |
| Word (.doc) | HTML Blob |

### PWA
- Embedded web app manifest with a gold crown "RK" icon
- "Install App to Desktop" button using the browser's native install prompt
- Offline support: click **Offline file (sw.js)** to download the service worker, then place it next to the HTML file

## Getting started

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Serve it locally, since installation needs `https` or `localhost`:
   ```bash
   python -m http.server 8000
   ```
3. Open `http://localhost:8000/rk-jewellery.html`.
4. Click **Install App to Desktop**, or use the browser menu and choose *Install app*.

### Hosting on GitHub Pages
Rename `rk-jewellery.html` to `index.html`, then go to **Settings → Pages** and deploy from the main branch. GitHub Pages serves over HTTPS, so the app can be installed from there.

## Tech stack
- HTML5, Tailwind CSS (CDN), Font Awesome 6 (CDN)
- Vanilla JavaScript
- [SheetJS](https://sheetjs.com/) and [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) (CDN)

The CDN libraries need an internet connection on first load.

## Project structure
```
rk-jewellery.html   # the whole app
sw.js               # optional offline service worker (downloaded from the app)
```

## License
Add your license here, for example MIT.

© RK Jewellery
