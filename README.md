# Oak Palm — Passive LP Teaser

One-pager for **Project Oak Palm**. A confidential passive LP opportunity. Distribution and email-gating handled by Jetty.

## Files

- `index.html` — web-viewable teaser (GitHub Pages entry point)
- `Oak-Palm-Teaser.pdf` — downloadable PDF, US Letter, 1 page
- `logos/` — brand logo assets
- `teaser.html` — synced duplicate of `index.html` (kept as fallback / direct-link source)

## Local preview

```bash
open index.html
```

## Regenerate the PDF

After editing `index.html`, re-render:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer \
  --print-to-pdf="Oak-Palm-Teaser.pdf" \
  --print-to-pdf-no-header \
  "file://$(pwd)/index.html"
```

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Initial teaser"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

Then in repo Settings → Pages → set Source to `main` / root. Live URL: `https://<user>.github.io/<repo>/`.

The "Download PDF" button on the page resolves to `Oak-Palm-Teaser.pdf` at the repo root.
