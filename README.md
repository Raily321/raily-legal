# Raily legal static pages

English-only Privacy Policy and Terms of Use for the Raily iOS app.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Landing page with links to both documents |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Use |

Contact used in the pages: `support@raily.app`  
Update dates are intentionally omitted from the published pages.

## Deploy with GitHub Pages

### Option A — publish this folder from a dedicated repo

1. Create a GitHub repository (public or private with Pages enabled on your plan).
2. Copy the contents of `legal-static/` to the repository root (so `index.html` is at `/`).
3. On GitHub: **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Choose branch `main` (or `master`) and folder **/ (root)**.
6. Save. After a minute or two, open the site URL shown on the Pages settings screen, for example:
   - `https://<user>.github.io/<repo>/`
7. Point the App Store / in-app Privacy Policy and Terms URLs to:
   - `https://<user>.github.io/<repo>/privacy.html`
   - `https://<user>.github.io/<repo>/terms.html`

### Option B — keep this folder inside a larger repo

1. Push the project that contains `Raily/legal-static/`.
2. In **Settings → Pages**, deploy from branch and set the folder to `/docs` **or** use a GitHub Action / `gh-pages` branch.
3. If Pages can only serve `/` or `/docs`, either:
   - copy these HTML files into `/docs`, or
   - use a custom workflow that publishes only `legal-static/` as the Pages artifact.

### Custom domain (optional)

1. In Pages settings, add your domain (for example `legal.raily.app`).
2. Add the DNS records GitHub shows (usually `CNAME` or `A`/`AAAA`).
3. Wait for HTTPS to become active, then use:
   - `https://legal.raily.app/privacy.html`
   - `https://legal.raily.app/terms.html`

## Local preview

Open `index.html` in a browser, or from this directory run:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`.

## Notes

- Pages are static HTML only; no build step is required.
- Keep App Store Connect privacy / support URLs in sync when the Pages URL changes.
- These documents are not a substitute for formal legal review.
