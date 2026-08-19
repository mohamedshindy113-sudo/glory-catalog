# GLORY 2026 Catalog — Deploy to GitHub Pages

This folder is a complete, ready-to-deploy static site (GitHub Pages compatible).
The git repo is already initialized with a clean commit on `main`; `.nojekyll` is present.

## One-command deploy (once GitHub auth is available)

```bash
cd "D:\Work\GLORY\brand\Catalouge\web"
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/glory-catalog.git
git push -u origin main
```

Then enable Pages (repo → Settings → Pages → Deploy from branch, `main`, `/root`)
or push an empty commit to trigger the Pages workflow. The site will be live at:

    https://<YOUR_GITHUB_USERNAME>.github.io/glory-catalog/

## Content

- `index.html` — single-page responsive catalog (lazy-loaded gallery, section nav,
  tap-to-zoom lightbox, floating WhatsApp order button to +201064128434)
- `images/page-001.jpg` … `page-065.jpg` — 65 web-optimized pages (~1000px, ~126KB avg, ~8.2MB total)
- `.nojekyll` — required so GitHub Pages serves raw files

## Rebuild from source PDF (if ever needed)

Source: `D:\Work\GLORY\brand\Catalouge\2026\GLORY-CATALOGUE-2026-LIGHT-150dpi-colorfix.pdf`
Extract with PyMuPDF (`fitz`): render each of 65 pages at ~1000px, JPEG quality ~80.
