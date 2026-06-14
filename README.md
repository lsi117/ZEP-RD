# Zones Enablement Portal

A static, interactive prototype of the Zones Enablement Portal — a learning &
sales-enablement product for technology sellers. This is a **single
self-contained file**: all app code, styles, IBM Plex fonts, media, and even
React/Babel are inlined into `index.html`. It works **offline** — no build step,
no server, no internet required.

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Put these two files in the repo root:

   ```
   index.html
   .nojekyll
   ```

3. Commit and push to the `main` branch.
4. In the repo: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)**
   - Save.
5. Wait ~1 minute, then open the URL GitHub shows, e.g.
   `https://<your-username>.github.io/<repo-name>/`

`index.html` is the entry point and loads automatically. (The `.nojekyll` file
isn't strictly required for a single file, but it's harmless and prevents Pages
from doing any Jekyll processing — keep it.)

## Notes

- **Fully self-contained / offline-capable:** you can also just double-click
  `index.html` to open it locally, or host it on any static host (Netlify,
  S3, an internal server) by uploading the one file.
- **Progress is saved locally:** lesson progress, theme, and the current screen
  persist in each visitor's browser `localStorage` (keys prefixed
  `zones-portal-`). It is per-browser, not synced.
- **Editing later:** this file is compiled. To make changes, edit the source
  project and re-export, rather than editing `index.html` by hand.
