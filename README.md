# aimedialab.github.io
Development of media lab 
# Deploying to https://aimedialab.github.io

This folder is a ready-to-publish GitHub Pages site (`index.html` + `css/style.css`).

## 1. Create the GitHub org

1. Go to https://github.com/account/organizations/new and create an org named **aimedialab**.
2. GitHub asks you to pick a plan — the free tier is fine for Pages.

## 2. Create the repo

Inside the `aimedialab` org, create a new repository named **exactly**:

```
aimedialab.github.io
```

The name has to match the org name for GitHub to auto-publish it at the root domain (`https://aimedialab.github.io`) instead of a subpath.

- Keep it public (Pages on the free tier requires a public repo, unless you're on GitHub Enterprise).
- Don't initialize with a README (you already have one here).

## 3. Push this folder

From this folder, run:

```bash
cd aimedialab-site
git init
git add .
git commit -m "Initial AI Multimedia Lab site"
git branch -M main
git remote add origin https://github.com/aimedialab/aimedialab.github.io.git
git push -u origin main
```

## 4. Enable Pages (usually automatic)

Repos named `<org>.github.io` publish automatically from the `main` branch root. If it doesn't show up within a minute or two:

1. Go to the repo → **Settings → Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Save.

Your site will be live at **https://aimedialab.github.io** shortly after.

## Editing later

- Copy: edit the text directly in `index.html`.
- Colors/fonts: edit `css/style.css` (`:root` variables at the top control the Wayne State green/gold palette).
- After any edit: `git add . && git commit -m "update" && git push`.
