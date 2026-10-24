# abilityenhancerapps.com

Static, information-only website for **Ability Enhancer Apps**. Plain HTML + CSS. No JavaScript, forms, cookies, trackers or external fonts.

## Pages
- `/` Home · `/speakmytalk/` · `/speakmytalk/guide/` · `/speakmytalk/privacy/` · `/accessibility/` · `/about/` · `404.html`

## Deploy on GitHub Pages
1. Sign in to GitHub as **abilityenhancerapps**. Create a public repository named `abilityenhancerapps.github.io` (or `website`).
2. Push this folder to the `main` branch:
   ```bash
   git remote add origin https://github.com/abilityenhancerapps/abilityenhancerapps.github.io.git
   git push -u origin main
   ```
3. Repository **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
4. **Custom domain**: enter `abilityenhancerapps.com` (the `CNAME` file already contains it).
5. At your domain registrar, add DNS records:
   | Type | Host | Value |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | abilityenhancerapps.github.io |
   Remove any other A/AAAA "parking" records for `@`. DNS can take up to 24-48 hours.
6. Back in Settings → Pages, tick **Enforce HTTPS** once it becomes available.
7. Recommended: verify the domain in GitHub (Settings → Pages → *Verified domains*) to prevent takeover.

## Editing
Pages are generated from a small Python script outside this repo; small edits can be made directly in the HTML files.
Links are root-relative (`/about/`), so preview with a local server: `python3 -m http.server` then open http://localhost:8000.
