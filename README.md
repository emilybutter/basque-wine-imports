# Basque Wine Imports

Marketing website for **Basque Wine Imports** — a Kansas City–based importer of indigenous-grape wines from the Atlantic Basque Country, founded by Dr. Kerri Lesh.

## Stack

Plain static HTML + CSS. No build step, no framework, no dependencies — drop the folder on any static host (Netlify, Vercel, Cloudflare Pages, GitHub Pages, S3 + CloudFront) and it works.

## Pages

| File          | Purpose                                                             |
|---------------|---------------------------------------------------------------------|
| `index.html`  | Home — hero, producer feature, wine grid, upcoming events           |
| `about.html`  | Kerri's story, credentials, the Topa mark, contact form, FAQ        |
| `wines.html`  | Full portfolio — two producers, six bottles, three grape field notes |
| `events.html` | Upcoming tastings, the 2027 Basque Country trip, past pours          |
| `blog.html`   | The Journal — index + 9 long-form posts (event previews, grape notes, travel) |
| `styles.css`  | Global design tokens, type scale, components                         |

## Design system

**Palette**

| Token      | Hex       | Usage                          |
|------------|-----------|--------------------------------|
| `--moss`   | `#8DA63F` | Accents, italics, focus rings  |
| `--forest` | `#2A4429` | Body text, dark sections       |
| `--sage`   | `#5A7152` | Muted secondary text           |
| `--mist`   | `#E6ECE0` | Surfaces, callouts             |
| `--rule`   | `#C8D2C0` | Hairline borders               |
| `--white`  | `#FFFFFF` | Page background                |

**Typography**

- Serif: **Libre Baskerville** (headings + body)
- Mono: **IBM Plex Mono** (labels, eyebrows, buttons, nav)

Italics inside headings (`<em>` / `<i>`) auto-color to moss green.

**Components in `styles.css`**

- `.btn` · `.btn--primary` · `.btn--secondary` · `.btn--tertiary` · `.btn--small` · `.btn--medium`
- `.btn .on-dark--primary` · `.on-dark--secondary` (for dark-green sections)
- `.nav-item` · `.nav-item--active`
- `.site-title` · `.header` · `.site-footer` · `.announcement-bar`
- `.newsletter-input`
- `.bwi-pill` · `.bwi-pill--moss` · `.bwi-pill--filled`

Page-specific layout lives in inline `<style>` blocks at the top of each HTML file. Shared tokens and component styles live in `styles.css`.

## Assets

- `assets/topa-logo.webp` — The Topa mark (ikurriña border + "Topa" Basque word for "cheers")
- `assets/basque-flag.png` · `assets/kc-flag.png` — Flags in the footer
- `assets/tech-sheets/*.pdf` — Wine spec sheets (Zura, Ilun, Gorka Izagirre, Zudugarai White/Rosé/Sparkling)
- Photography: Kerri's portraits, the Vicia Wine Garden, Bar Vin storefront, the women-in-wine cheese spread, the 2027 trip map, the Gorka Izagirre lineup, etc.

## External image references

A few hero images on `blog.html` and `index.html` are still hot-linked from Kerri's existing Squarespace CDN (`images.squarespace-cdn.com/...`). To go fully self-hosted, download those images locally and update the `background-image` URLs.

## Forms

The contact form on `about.html` uses `<form action="mailto:kerri@basquewineimports.com">`. For production, wire it to a real form handler (Formspree, Netlify Forms, or a serverless function) — `mailto:` works but isn't reliable.

## Newsletter signup

The footer newsletter input is currently a static stub. Wire it to Mailchimp, Buttondown, ConvertKit, or whichever provider Kerri uses for the monthly journal letter.

## License & content

Site code: free to reuse and modify.
Photography, copy, and the Topa mark belong to Basque Wine Imports.
