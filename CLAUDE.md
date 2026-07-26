# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Deployment

This project is hosted on Cloudflare. **After every change, always deploy immediately:**

```
wrangler deploy
```

Run this from `f:\claude workspace\projects\fraction calculator`. Do not wait for the user to ask — deploying is part of completing any task. Never tell the user to refresh until after the deploy has run successfully.

## Architecture

Single-file app: everything lives in `index.html`. No build step, no bundler, no dependencies. Edit `index.html` directly.

Hosted as Cloudflare Pages static assets (`wrangler.json` → `assets.directory: "./"`).

## Git workflow

Solo project. Push directly to main — no pull requests unless the user explicitly asks.
