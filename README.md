# CC project

This is a small static website consisting of `index.html`, `about.html`, and `style.css`.

## Build

- There is no build step — the site is plain HTML/CSS and can be opened directly in a browser.

## Serve locally

Options to view the site locally from the project folder (macOS / zsh):

- Open the `index.html` file in the default browser:

```bash
open index.html
```

- Start a simple Python HTTP server (recommended for testing relative requests):

```bash
# using Python 3
python3 -m http.server 8000
# then open http://localhost:8000
```

- Using Node (no global install):

```bash
# one-off with npx
npx serve . -l 8000
# or
npx http-server . -p 8000
```

## Optional: npm script for convenience

If you want `npm start` to run a local server, create a `package.json` and install `serve` or `http-server` as dev dependency:

```bash
npm init -y
npm install --save-dev serve
```

Then add this to `package.json` under `scripts`:

```json
"scripts": {
  "start": "serve . -l 8000"
}
```

Now run:

```bash
npm start
```

## Deploy

- GitHub Pages: push the repository to GitHub and enable Pages from the repository settings (branch `main` or `gh-pages`). For a project site, you can use the `gh-pages` branch or the `gh-pages` npm package to publish.

- Netlify: connect the repo to Netlify (drag & drop the folder in the Netlify UI or link the repo). No build command required — set publish directory to `/` or the repo root.

- Vercel: import the repo into Vercel and deploy. Vercel automatically detects static projects; no build settings are required.

## Next steps (suggested)

- Add a `README.md` (this file) — done.
- If you want automated deployment, I can add a simple GitHub Actions workflow, or scaffold `package.json` + `start` script for local convenience.

---

If you want, I can also:
- Add `package.json` and `npm start` now
- Create a GitHub Actions workflow for GitHub Pages
- Set up a Netlify `_redirects` or configuration file if needed

Tell me which of the above you'd like me to do next.