# Nate Michaels

Personal brand site for **Nate Michaels** — human geography, cultural geography, international
travel, living abroad, and the systems connecting places, people, and everyday life.

Static HTML/CSS/JS. No build step, no framework, no dependencies beyond a Google Fonts link.

## Files

```
index.html            # all page content and sections
assets/css/style.css   # editorial design system (colors, type, layout)
assets/js/main.js      # mobile nav toggle + footer year
README.md
```

## Local preview

No build step is required. From the repository root, run either:

```bash
# Option A: just open it
start index.html          # Windows
open index.html           # macOS

# Option B: serve it locally (recommended, avoids any relative-path quirks)
python -m http.server 8000
# then visit http://localhost:8000
```

## Publishing to GitHub Pages

1. Push this repository to GitHub (repo: `bentley-michael/nate-michaels`).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Choose the branch (e.g. `main`) and folder `/ (root)`, then save.
5. GitHub Pages will publish at `https://bentley-michael.github.io/nate-michaels/`.

All internal links and asset references use relative paths (e.g. `./assets/css/style.css`), so
the site works identically at the GitHub Pages subpath or at a future custom domain — no changes
needed either way.

### Custom domain (optional, future)

A `CNAME` file is intentionally omitted. Add one only when a custom domain (e.g.
`natemichaels.us`) is ready to be pointed at this repo.

## Editing content

Everything lives in `index.html`, organized into clearly commented `<section>` blocks:

- **Explore** (`#explore`) — the four topic cards. Edit copy directly in the `.topic-card` items.
- **Field Notes** (`#field-notes`) — the coffee field note links to its article page; the remaining
  `.post-card` items are placeholders until their articles are published.
- **Tools & Guides** (`#tools`) — product cards in `.product-card` items. Update price, benefit
  bullets, and the Payhip link (`href`) as products change.
- **About** (`#about`) — plain paragraphs, safe to edit freely.
- **Newsletter** (`#newsletter`) — one CTA button, linked to the Nate Michaels Substack profile.

Styling lives in `assets/css/style.css`; behavior (mobile nav + footer year) lives in
`assets/js/main.js`. Neither needs to change for routine content edits.

