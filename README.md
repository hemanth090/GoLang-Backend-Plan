# Go Backend in 30 Days

> Interactive 4-week plan to go from zero to a production-shaped Go backend. HTTP APIs, Kafka, Postgres, Redis, notifications, Snowflake, and Databricks. Progress saves locally in the browser.

Live: deploy `dist/` to **Vercel** or **Netlify** in one click. Static Astro, no backend required.

## Preview

- 4 weeks, 28 days, 84 checkable tasks, 20 quiz questions
- Progress + quiz state in `localStorage` (`go-backend-plan-v1`)
- Full-bleed editorial UI, Geist + Geist Mono (Supermemory lineage), YC-backed calm

## Tech Stack

- **Astro 5** (static, `src/pages/index.astro` single-file app)
- **Vanilla JS** + `localStorage`
- **Geist** via Google Fonts (`Geist:wght@400;500;600` + `Geist Mono:wght@400;500`)
- No frameworks, no UI libs

## Getting Started

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # → dist/
npm run preview  # serve dist
```

Requires Node 20+.

## Project Structure

```
.
├── src/
│   └── pages/index.astro   # plan data + template + script + styles (single file)
├── public/                 # static assets (empty)
├── astro.config.mjs
├── vercel.json             # Vercel: build → dist
├── netlify.toml            # Netlify: build → dist
└── package.json
```

All week/day/task/quiz content lives at the top of `src/pages/index.astro:31-693`. Edit there, rebuild.

## Deployment

### Vercel (recommended)
1. Push to GitHub
2. [vercel.com/new](https://vercel.com/new) → Import repo → Framework `Astro` auto-detected → Deploy
3. Build command `npm run build`, output `dist` (see `vercel.json`)

Or via CLI:
```bash
npm i -g vercel
vercel --prod
```

### Netlify
1. Push to GitHub → [app.netlify.com](https://app.netlify.com) → Add new site → Import → Deploy
2. Build `npm run build`, publish `dist` (see `netlify.toml`)

Or drag `dist/` to Netlify manual deploy, or:
```bash
npm i -g netlify-cli
netlify deploy --prod --dir=dist
```

### GitHub Pages
Build locally and publish `dist/` to `gh-pages` branch, or use `withastro/action`.

## Customization

- **Content:** edit `plan` array in `src/pages/index.astro:31`
- **Fonts:** Google Fonts link at `src/pages/index.astro:708`
- **Tokens:** `:root` at `src/pages/index.astro:1005` — `--bg`, `--line`, `--text`, `--radius-*`, `--ease`
- **Layout:** hero/tabs/main/footer are full-bleed with `clamp(16px,4vw,40px)` padding; days become 2-col at `≥1100px`

## Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Dev server |
| `npm run build` | Static build to `dist/` |
| `npm run preview` | Preview production build |

## License

MIT — do what you want.
