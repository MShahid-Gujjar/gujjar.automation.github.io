# Freelance Engineer Website

Static one-page site: Qt/C++/QML, EV charging (OCPP), and Siemens TIA Portal / PLC automation
freelance services. No build step, no framework — plain HTML/CSS/JS.

## Files

```
index.html      Page content
css/style.css   Styling (light + dark mode via prefers-color-scheme)
js/script.js    Mobile nav toggle + footer year
```

## Placeholders to replace before publishing

All dummy content lives in `index.html`. Search for these and swap in your real details:

| What | Where | Current placeholder |
|---|---|---|
| Name | `<title>`, logo, hero, footer | `Max Mustermann` |
| Photo | hero section, `.hero-photo` | SVG silhouette — replace with `<img src="assets/your-photo.jpg" alt="Your Name">` |
| Email | Contact section (x2) | `max.mustermann@example.com` |
| Phone | Contact section | `+43 000 0000000` |
| GitHub | hero button + Profiles section | `https://github.com/YOUR-GITHUB-USERNAME` |
| LinkedIn | Profiles section | `https://www.linkedin.com/in/YOUR-LINKEDIN-ID` |
| Upwork | Profiles section | `https://www.upwork.com/freelancers/~YOUR-UPWORK-ID` |
| Freelancer.com | Profiles section | `https://www.freelancer.com/u/YOUR-FREELANCER-ID` |
| Malt | Profiles section | `https://www.malt.at/profile/YOUR-MALT-ID` |
| Xing | Profiles section | `https://www.xing.com/profile/YOUR-XING-ID` |
| Portfolio projects | Portfolio section (x3 cards) | generic placeholder text |

If you don't have a profile on one of the freelance platforms (Upwork, Freelancer.com, Malt,
Xing), just delete that `<a>` line from the Profiles section.

To add your photo: drop a JPG/PNG into `assets/`, then in `index.html` replace the `<svg>...</svg>`
block inside `.hero-photo` with `<img src="assets/your-photo.jpg" alt="Your Name">` and remove the
`.photo-badge` span.

## Preview locally

Any static file server works, e.g.:

```
py -m http.server 5050
```

Then open http://localhost:5050.

## Free hosting

**GitHub Pages (recommended — you already have a free GitHub account):**

1. Create a new public repo on GitHub, e.g. `yourname.github.io` (using your exact GitHub
   username gives you a clean root URL) — or any repo name if you're fine with a `/reponame/`
   path.
2. Push these files to it:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. On GitHub: repo → Settings → Pages → Source: "Deploy from a branch" → Branch: `main` / `root`
   → Save.
4. Your site goes live at `https://YOUR-USERNAME.github.io/` (or `/YOUR-REPO/` for a non-root
   repo name) within a minute or two.
5. Optional: add a custom domain later under Settings → Pages → Custom domain.

**Alternatives (also free, and arguably even simpler — drag-and-drop, no git required):**

- **Netlify** (netlify.com) — drag the project folder onto the Netlify "Deploy" dashboard, or
  connect the GitHub repo for auto-deploys on push. Free custom subdomain, easy custom domain
  later.
- **Vercel** (vercel.com) — same idea as Netlify, connect the GitHub repo and it deploys
  automatically.
- **Cloudflare Pages** (pages.cloudflare.com) — connect the GitHub repo, fast global CDN, free
  tier is generous.

All four are genuinely free for a static site like this (no backend, no database). GitHub Pages
is the easiest starting point since you already have the account and it keeps hosting and source
code in the same place.
