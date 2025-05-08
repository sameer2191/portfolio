# Sameer Mir Portfolio - Production Deployment Guide

This guide will help you deploy your portfolio website with maximum reliability and no CDN dependencies (fonts, icons, Tailwind CSS are all local).

---

## 1. Project Structure

```
portfolio/
├── dist/
│   └── output.css              # Built Tailwind CSS
├── fonts/
│   ├── Satoshi-Regular.woff2
│   ├── Satoshi-Medium.woff2
│   ├── Satoshi-Bold.woff2
│   ├── Inter-Variable.ttf
│   └── fontawesome/
│       ├── fa-solid-900.woff2
│       ├── fa-regular-400.woff2
│       ├── fa-brands-400.woff2
│       └── all.min.css
├── src/
│   └── input.css               # Tailwind + font-face declarations
├── index.html
├── package.json
├── tailwind.config.js
└── README.md
```

---

## 2. Download & Place Font Files

#### Satoshi (Fontshare)
- [Satoshi Regular (400) WOFF2](https://cdn.fontshare.com/wf/TTX2Z3BF3P6Y5BQT3IV2VNOK6FL22KUT/7QYRJOI3JIMYHGY6CH7SOIFRQLZOLNJ6/KFIAZD4RUMEZIYV6FQ3T3GP5PDBDB6JY.woff2)
- [Satoshi Medium (500) WOFF2](https://cdn.fontshare.com/wf/P2LQKHE6KA6ZP4AAGN72KDWMHH6ZH3TA/ZC32TK2P7FPS5GFTL46EU6KQJA24ZYDB/7AHDUZ4A7LFLVFUIFSARGIWCRQJHISQP.woff2)
- [Satoshi Bold (700) WOFF2](https://cdn.fontshare.com/wf/LAFFD4SDUCDVQEXFPDC7C53EQ4ZELWQI/PXCT3G6LO6ICM5I3NTYENYPWJAECAWDD/GHM6WVH6MILNYOOCXHXB5GTSGNTMGXZR.woff2)

#### Inter (Google Fonts)
- [Inter Variable (TTF)](https://github.com/rsms/inter/releases/download/v4.0/Inter-VariableFont_slnt,wght.ttf)
  - Download and rename to `Inter-Variable.ttf`

#### Font Awesome 6.5.2
- [fa-solid-900.woff2](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/webfonts/fa-solid-900.woff2)
- [fa-regular-400.woff2](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/webfonts/fa-regular-400.woff2)
- [fa-brands-400.woff2](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/webfonts/fa-brands-400.woff2)
- [all.min.css](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css)

---

## 3. Install Dependencies & Build CSS

```
npm install
npm run build:css
```
- This will generate `dist/output.css` for production use.

---

## 4. Deploy

- Deploy the contents of your project (including `dist/`, `fonts/`, `index.html`, etc.) to Netlify, Vercel, or any static host.
- Your site will use only local fonts, icons, and CSS. No CDN dependencies for critical assets.

---

## 5. Troubleshooting
- If you see default fonts or missing icons, double-check that all font files are present and paths match exactly.
- If you update Tailwind config or CSS, re-run `npm run build:css`.

---

## 6. Credits
- Satoshi font by Indian Type Foundry (Fontshare)
- Inter font by Rasmus Andersson
- Font Awesome by Fonticons, Inc.
- Tailwind CSS

---

For any issues, open your browser dev tools and check the Network tab for missing files or 404s.
