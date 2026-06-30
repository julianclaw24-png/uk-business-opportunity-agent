# Opportunity Pipeline OS

A static webpage for turning AI-discovered business ideas into an execution pipeline.

## What it does

- Loads fresh opportunities from `data/latest-report.json`
- Seeds them into a staged workflow board
- Lets you move opportunities through stages:
  - Inbox
  - Qualify
  - Outreach
  - Validating / Offer shaping
  - Offer Ready / Live
  - Won / Parked
- Lets you edit notes, thesis, next step, and conviction
- Saves state in browser local storage
- Supports export/import of board state so you can move it between devices

## Run locally

From this folder:

```bash
python3 -m http.server 8091 --bind 0.0.0.0
```

Then open:

- `http://localhost:8091`
- or from another device on your network: `http://YOUR-IP:8091`

## Access from anywhere

Because this is a static site, you can host it almost anywhere:

- GitHub Pages
- Netlify
- Cloudflare Pages
- Your own VPS / Docker / Nginx

## Important note about sync

Current MVP persistence is browser-local by default.

That means:
- the page itself can be accessed from anywhere once hosted
- but edits do **not** automatically sync across devices yet

For true anywhere editing with shared state, next step is adding:
- Supabase
- Firebase
- or a tiny authenticated backend/API

## Files

- `index.html` — main application
- `data/latest-report.json` — latest AI opportunity feed

## Suggested next upgrade

Add login + cloud sync so the pipeline state follows you across phone, laptop, and tablet.
