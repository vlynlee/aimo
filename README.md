# AIMO — band site

Static site for AIMO (robot emo / post-hardcore). Plain HTML — no build step.

- `index.html` / `AIMO-Home.html` — home
- `AIMO-Music.html`, `AIMO-Videos.html`, `AIMO-Band.html`, `AIMO-Contact.html`
- `AIMO-Echo.html`, `AIMO-Byte.html`, `AIMO-Glitch.html`, `AIMO-Static.html` — member pages
- `assets/` — images · `support.js`, `image-slot.js` — runtime

## View locally
Open `index.html` in a browser (needs internet for the Google Fonts).

## Put it on a private GitHub repo
1. On github.com → **New repository** → name it (e.g. `aimo-site`), set **Private**, create.
2. Upload: on the empty repo page click **uploading an existing file**, then drag in *everything in this folder* (index.html, the AIMO-*.html files, `assets/`, `support.js`, `image-slot.js`, this README). Commit.
   - Or via CLI: `git init && git add . && git commit -m "AIMO site" && git branch -M main && git remote add origin <your-repo-url> && git push -u origin main`
3. Invite your reviewer: repo **Settings → Collaborators → Add people** → their GitHub username. They get read access; the repo stays private to everyone else.

## Let them SEE the live site privately
GitHub Pages on a free account would make the *live* URL public (repo stays private, but anyone with the link can view). If that's fine, enable **Settings → Pages → Deploy from branch → main → /(root)**.

For a truly private live URL (recommended):
1. **Cloudflare Pages** → Create project → connect your GitHub repo → Framework preset: **None** → build command: *(empty)* → output dir: `/`.
2. After it deploys, go to **Cloudflare Zero Trust → Access → Applications → Add self-hosted app**, point it at the Pages URL, add an **Allow** policy limited to your reviewer's email. Now only that email (after a one-time email code) can open the site.

Both are free.
