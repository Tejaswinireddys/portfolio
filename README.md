# Portfolio — Tejaswini Reddy Sodanapalli

Personal portfolio site for **Tejaswini Reddy Sodanapalli** — Senior Software Engineer specialising in AI Platform Engineering, MLOps, and large-scale distributed systems.

**Live:** [tejaswini-reddy.pplx.app](https://tejaswini-reddy.pplx.app)

## Stack

- Plain HTML + CSS (no build step, no framework)
- Inter + JetBrains Mono + Instrument Serif (Google Fonts)
- Inline SVG logo, no external JS dependencies
- Fully responsive (390px → 1280px+)
- Dark-mode-first design

## Project structure

```
portfolio/
├── index.html      # All content lives here
├── styles.css      # Design tokens + layout
└── README.md
```

## Local preview

No dependencies — just open `index.html` in a browser, or:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Editing guide

| Want to change…             | Edit                                                        |
| --------------------------- | ----------------------------------------------------------- |
| Hero headline / tagline     | `index.html` → `.hero-h1`, `.hero-sub`                      |
| Stats (years, repos, etc.)  | `index.html` → `.hero-stats`                                |
| Featured projects           | `index.html` → `<section id="projects">` → `.project` cards |
| Work experience             | `index.html` → `<section id="experience">` → `.timeline`    |
| Tech stack                  | `index.html` → `<section id="stack">` → `.stack-card`       |
| Contact details             | `index.html` → `<section id="contact">`                     |
| Colours / typography / spacing | `styles.css` → `:root` design tokens                     |

### Design tokens

All colours, fonts, radii, and spacing live as CSS variables in the top of `styles.css`:

```css
:root {
  --bg: #0a0b0d;
  --accent: #00e5a8;
  --text: #e7ecf2;
  --font-sans: 'Inter', ...;
  --font-serif: 'Instrument Serif', ...;
  ...
}
```

Tweak one variable to reskin the whole site.

## Deploying updates

The site is hosted on `pplx.app`. To update the live site:

1. Edit `index.html` / `styles.css`
2. Commit + push to GitHub
3. Re-deploy via Perplexity Computer (or wire up your own CI to publish elsewhere — see "Hosting elsewhere" below)

## Hosting elsewhere

This is a fully static site — drop it on any static host:

- **GitHub Pages** — push to a `gh-pages` branch or `main` and enable Pages in repo settings
- **Vercel / Netlify** — connect the repo, no build command, output directory `/`
- **Cloudflare Pages** — same deal, no build step

## License

Personal portfolio — content © Tejaswini Reddy Sodanapalli. Code released as-is for reference.
