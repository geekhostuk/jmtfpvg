# JMT FPV — Shutdown Notice

A single-page closure notice for the JMT FPV League, built with [Astro](https://astro.build)
and hosted on Cloudflare Pages. Imported from the Claude Design project
*"JMT FPV Shutting Down"*.

## Develop

```bash
npm install
npm run dev      # http://localhost:4321
```

## Build

```bash
npm run build    # outputs static site to ./dist
npm run preview  # preview the production build locally
```

## Deploy to Cloudflare

The site is fully static, so it deploys to **Cloudflare Pages** with no adapter.

### Option A — Wrangler (from this machine)

```bash
npm run deploy   # runs `astro build` then `wrangler pages deploy ./dist`
```

The first deploy will prompt you to log in and create/select a Pages project.

### Option B — Git integration (recommended)

Connect the repo in the Cloudflare dashboard → Pages → *Create application* and set:

- **Build command:** `npm run build`
- **Build output directory:** `dist`
- **Framework preset:** Astro

## Editing content

Page copy, stats, and links live in `src/pages/index.astro`:

- `noticeDate` — the date shown in the eyebrow ("Service Notice · …").
- `githubUrl` — the "Get the code on GitHub" button.
- `contactUrl` — the "feel free to reach out" link.
- `stats` — the by-the-numbers grid.
