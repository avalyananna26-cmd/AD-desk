# AD Desk

Pre-production for first assistant directors. AD Desk turns a screenplay into a shooting plan:

- **Breakdown**: scene numbers, page eighths, and colour-coded tags for cast, extras, props, wardrobe, vehicles and effects.
- **Hidden scenes**: one written scene that is really several setups gets split into 2A, 2B…
- **Versions**: save a change as an update, 1.1 or 2; the breakdown carries over.
- **Cast & locations**: actor schedules per day (not available, busy hours, free only), location dates and hours.
- **Call sheets**: pick scenes from the breakdown; clashes with cast and location availability are flagged.
- **Sides**: the day's script pages for each actor, with their own scenes marked.

## How it runs

AD Desk is one HTML file (`index.html`) with no build step and no server.

- **On this website** (Netlify), everything is saved in the visitor's browser (localStorage). The two sample scripts include their scene splits; other scripts are split by hand.
- **Inside Claude** (as a Claude artifact), the same page also signs people in with their Claude account, stores scripts in that account, detects hidden scenes with Claude, and can email sides through Gmail.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Deploy

Connected to Netlify: every push to `main` publishes the site. Settings live in `netlify.toml` (publish directory `.`, no build command).

Built by Anna Avalyan as a vibe-coding class project, with Claude.
