# Shadrack Safari — portfolio, live CV and sales page

One HTML file. No build step. Based on the structure, palette and GSAP scroll
motion of the free **Linea** template by 8B (MIT licence).

## What's in here

```
index.html          the whole site — markup, styles, config and motion
assets/shots/       real screenshots of your three live sites (used in the mockup)
assets/hero.jpg     optional: drop a wide photo of yourself here
LICENSE             MIT
```

## Editing anything (the config)

Everything personal lives in one `SITE` object at the top of the `<script>`
block near the bottom of `index.html`, clearly marked:

- your name, role, location
- email + WhatsApp number (every link on the page is generated from it)
- the three projects: name, category, live URL, screenshot, blurb, feature tags
- the trust row under the hero ("3 live sites / 3 skill areas / 24h reply")
- skill tags shown in the Skills preview panel

Text you can edit directly in the HTML: section headings, the "You ask / I
deliver" pairs, FAQ answers, the three buying steps, and the testimonial
placeholder cards (replace `[A line a client actually said]` with real quotes
only).

### Adding your photo

Put a wide photo (1600 px wide or more) at `assets/hero.jpg`. It appears
behind the hero with a dark overlay. Without it, a painted sunset gradient is
used — the page never looks broken.

### Refreshing the site screenshots

The three screenshots in `assets/shots/` are real captures of the live sites.
To retake them after a redesign, open each site in a browser at 1600 × 1000,
take a screenshot of the top of the page and save it over the matching file
(`bahari.jpg`, `foundora.jpg`, `olitech.jpg`).

## Run it locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 3000
# → http://localhost:3000
```

## Deploy on Vercel

1. Push this folder to your GitHub repo (`bahariasilisafaris/Portfolio`).
2. On [vercel.com](https://vercel.com) click **Add New → Project** and import
   the repo.
3. Leave everything on defaults — Vercel serves it as a static site:
   - Framework Preset: **Other**
   - Build Command: *(leave empty)*
   - Output Directory: *(leave empty / `.`)*
4. Click **Deploy**. Your site is live on a `*.vercel.app` URL in under a
   minute. Add a custom domain under **Settings → Domains** if you want one.

Redeploying: every push to `main` redeploys automatically.

## How it's built

- **Linea palette** — warm paper `#faf5f0`, espresso `#1b1411`, sand `#eee5dc`,
  navy `#1f3954`, one green accent `#33cc7a`. All colours are CSS variables;
  light/dark themes swap them on `<html data-theme>`.
- **Type** — Host Grotesk (Google Fonts), big tightly-tracked headlines.
- **Motion** — GSAP 3.13 + ScrollTrigger + Lenis smooth scroll (CDN). Pinned
  "You ask / I deliver" stage, sticky browser mockup that swaps sites as you
  scroll, pinned horizontal "In the room" track, stacking steps cards, green
  bar wipe on the closing headline, custom cursor with trailing ring, magnetic
  buttons and card tilt on desktop.
- **Honest by design** — no invented stats, clients or reviews. Testimonials
  are labelled placeholder cards until real quotes arrive.
- **Accessible** — keyboard-reachable everything, visible focus rings, native
  `<details>` FAQ, and `prefers-reduced-motion` turns all motion off while
  keeping the full page visible.

## Credits

Layout, spacing and animation style based on the
[Linea template by 8B](https://8b.com/templates/linea/) (MIT). Fonts: Host
Grotesk (OFL). Motion: GSAP (free, since 3.13) and Lenis (MIT).
