# TPC @ IJCAI 2026 — The 2nd Travel Planning Challenge with Agentic AI

Static website for the TPC 2026 challenge, co-located with IJCAI-ECAI 2026 in Bremen.

## Deploy to GitHub Pages

1. Create a new repo `IJCAI2026` under your GitHub org/user.
2. Copy the contents of this folder (including the hidden `.nojekyll` file) to the root of the repo.
3. Commit and push to the `main` branch.
4. In the repo, open **Settings → Pages**, set the source to **Deploy from a branch**, pick `main` / `/ (root)`, and save.
5. Wait about a minute. The site will be live at `https://<org-or-user>.github.io/IJCAI2026/`.

The `.nojekyll` file disables Jekyll processing so everything is served as-is.

## Files

| File | Purpose |
|---|---|
| `index.html` | Entry point. Contains the entire stylesheet and theme tokens. |
| `app.js` | Main React application (pre-compiled from JSX). |
| `tweaks-panel.js` | Floating Tweaks panel (theme, hero visual, sections). |
| `.nojekyll` | Disables Jekyll on GitHub Pages. |

## Local preview

Any static server works. For example:

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Registration

The registration buttons link to the Google Form configured as `registrationFormUrl` near the top of `app.js`.

## Updating the site

The source lives as JSX (`app.jsx`, `tweaks-panel.jsx`) in the design project. After any edit, re-compile to plain JS — Babel standalone is the simplest way:

```html
<!-- One-off compile in the browser, or use @babel/cli on the command line -->
```

Or run:

```bash
npx @babel/cli app.jsx --presets=@babel/preset-react -o app.js
npx @babel/cli tweaks-panel.jsx --presets=@babel/preset-react -o tweaks-panel.js
```

## License

Content © 2026 TPC organizers.
