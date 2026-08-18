# idanfranco.com

Personal academic website for Idan Franco. Built with [Quarto](https://quarto.org/) and deployed via GitHub Pages.

## Local preview

```bash
quarto preview
```

Opens a live-reloading preview at http://localhost:port.

## Render once

```bash
quarto render
```

Outputs to `_site/`.

## Deployment

Pushes to `main` automatically render and deploy the site via the GitHub Actions workflow in `.github/workflows/publish.yml`.

## Structure

```
.
├── _quarto.yml          # Site config: nav, footer, theme
├── styles.css           # Custom CSS (Chagai-inspired)
├── index.qmd            # Homepage with hero + bio
├── research.qmd         # Research projects by theme
├── publications.qmd     # Peer-reviewed + working papers
├── book.qmd             # Bloomsbury book project
├── teaching.qmd         # Teaching statement + courses
├── img/                 # Headshot, favicon
├── files/               # CV PDF, replication files
├── CNAME                # Custom domain for GitHub Pages
└── .github/workflows/   # Auto-deploy
```

## To-do before publishing

- [ ] Replace `img/headshot.jpg` with actual headshot (recommended: 1200×1500 px, neutral background)
- [ ] Add `img/favicon.png` (32×32 or 64×64 px)
- [ ] Add `files/cv.pdf`
- [ ] Replace placeholder URLs in `_quarto.yml` footer (Twitter, Google Scholar, LinkedIn)
- [ ] Fill in real publication details in `publications.qmd`
- [ ] Fill in book details in `book.qmd`
- [ ] Update Google Scholar / ORCID / Twitter URLs in `index.qmd`
- [ ] Set up custom domain (see below)

## Connecting idanfranco.com

1. In GitHub repo settings → Pages → Custom domain: `www.idanfranco.com`
2. In Wix (or wherever your DNS lives) add these records:
   - **A records** for `idanfranco.com` pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **CNAME record** for `www` pointing to `idanf2.github.io` (replace with your GitHub username)
3. Wait 1–24 hours for DNS propagation
4. In GitHub Pages settings, enable "Enforce HTTPS"
