# GitHub Pages setup for `schweinefilet.github.io`

This repository contains a simple redirect at `/boulderingelo/` that points to the existing project at:

`https://schweinefilet.github.io/BoulderingELO/`

Steps to publish this repo and enable GitHub Pages:

1. Commit the new files locally:

```bash
git add boulderingelo/index.html PAGES_SETUP.md
git commit -m "Add boulderingelo redirect and Pages instructions"
```

2. Create the user-site repository and push (using GitHub CLI) — replace `Schweinefilet` with your GitHub username if different:

```bash
# create the repo on GitHub and push current branch
gh repo create Schweinefilet/schweinefilet.github.io --public --source=. --remote=origin --push
```

If you prefer the web UI: create a new repository named `schweinefilet.github.io` (public), then add this repo as a remote and push.

3. Enable GitHub Pages (if not already enabled):

- In the repository on GitHub go to `Settings` → `Pages`.
- Under `Source` choose `main` branch (or the branch you pushed) and `/ (root)` folder, then Save.

4. Wait a minute for Pages to publish. Visit:

`https://schweinefilet.github.io/boulderingelo/`

You should be redirected to `https://schweinefilet.github.io/BoulderingELO/`.

Notes:
- The redirect uses a fast `meta refresh` with a JS fallback. If you need an HTTP 301 redirect instead, set up a small server or use redirects configured via GitHub Actions.
- This repository only provides a lowercase path (`/boulderingelo/`) that redirects to the uppercase project URL; the original site remains at `/BoulderingELO/`.
