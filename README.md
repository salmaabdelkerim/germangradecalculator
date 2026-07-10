# Notenrechner Uni

A standalone, no-dependency grade calculator for the German university scale (1.0–5.0).
Just two static HTML files — no build step, no backend, no framework.

## Files

- `index.html` — the calculator + explanatory content (this is your whole site)
- `impressum.html` — legally required Impressum template (German law, § 5 TMG). **Edit this before going live** — replace the bracketed placeholders with your real name and address.

## Deploy it (pick one, all free)

### Option A — Vercel (recommended, easiest)
1. Go to vercel.com, sign up with GitHub.
2. Create a new GitHub repo, push these two files to it.
3. In Vercel, "Add New Project" → import the repo → deploy. No config needed for plain HTML.
4. You get a free `*.vercel.app` URL immediately. Add your own domain later under Project → Settings → Domains.

### Option B — Netlify
1. Go to netlify.com → "Add new site" → "Deploy manually".
2. Drag the folder containing `index.html` and `impressum.html` straight into the browser.
3. Done — you get a free `*.netlify.app` URL instantly, no GitHub required.

### Option C — GitHub Pages
1. Push the files to a GitHub repo.
2. Repo Settings → Pages → set source to the `main` branch, root folder.
3. Site goes live at `https://yourusername.github.io/reponame`.

## Buying a domain

Once you're happy with the free URL, buy a domain (Namecheap, Porkbun, or IONOS if you want a German registrar) and point it at your host:
- Vercel/Netlify: add the domain in their dashboard, they give you DNS records to add at your registrar.
- Takes a few hours to propagate.

## Before you go live

1. **Edit `impressum.html`** — fill in your real name and address. This is a legal requirement in Germany, not optional, even for a free hobby site.
2. If you add ads or affiliate tracking, add a `Datenschutzerklärung` (privacy policy) page too — required as soon as you use any tracking/analytics/ad cookies.
3. Update the `<title>` and `<meta name="description">` in `index.html` if you rename the site or pick a different domain/niche.

## Extending it

Everything lives in one `<script>` tag at the bottom of `index.html` — plain JavaScript, no framework. Natural next features:
- A "Wunschnote" mode: given your current grade, calculate what you need on the last exam.
- Save/restore state via `localStorage` so returning visitors don't retype everything.
- Support for the Swiss (1–6, best-is-highest) or Austrian scale as a toggle, if you want to widen the audience.
