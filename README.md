# NYELETI.30 — Dress Heist Picker

A pop-art / Met-Gala / garage-sale-flyer one-pager to help Nyeleti pick a dress
for her 30th birthday dinner & drinks (Tue, 12 May 2026).

## Sizes
Picker is set for **XS / S**. If neither size is in stock, the look is shown
greyed out with a `NO XS/S` stamp and excluded from the spin-the-wheel.

## What's inside
- `index.html` — single static page. No build step.
- 15 dresses pulled from Vera's Closet & YDE.
- Filters: All / Available only / Favourites · plus 🎰 random pick + ♥ favourites
  saved in `localStorage`.

## Run locally
Just open `index.html` in any browser.

## Deploy to GitHub Pages (free hosting)

```bash
cd /Users/katlig/spoiltDress
git init -b main
git add index.html README.md
git commit -m "feat: nyeleti's 30th dress picker"

# Create a public repo (using GitHub CLI):
gh repo create nyeleti-30 --public --source=. --remote=origin --push

# Enable GitHub Pages on the main branch root
gh api -X POST repos/:owner/nyeleti-30/pages -f 'source[branch]=main' -f 'source[path]=/'
```

Site lives at: `https://<your-github-username>.github.io/nyeleti-30/`
First build takes ~30–60 seconds. Send Nyeleti the link.

### No `gh` CLI? Manual route:
1. Create a new public repo on github.com called `nyeleti-30`.
2. `git remote add origin git@github.com:<user>/nyeleti-30.git && git push -u origin main`
3. Repo → **Settings → Pages → Source:** `Deploy from a branch` → `main` / `/ (root)` → Save.

## Refreshing data
Stock changes daily — re-run the scrape script if you want fresh availability
the morning of the dinner. (Quickest: just check the live links from the page.)
