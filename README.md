# Personal Academic Website

A single-page academic homepage in the style of
[jonbarron.github.io](https://github.com/jonbarron/jonbarron.github.io).

## Files
- `index.html` — the page content (bio + publications)
- `style.css` — styling
- `images/` — profile photo + one thumbnail per paper (currently SVG placeholders)
- `Alexey_Kravets_CV.pdf` — add your CV here so the "CV" link works

## Preview locally
Open `index.html` in a browser, or run a local server:
```bash
cd page
python3 -m http.server 8000
# visit http://localhost:8000
```

## Replace placeholders
The `images/` folder contains placeholder SVGs. Swap them for real images:
- `profile.svg` → a square headshot (`profile.jpg` — then update the `src` in `index.html`)
- `sae / fewshot / forgetting / synthetic / calibration / overlap` → a teaser figure per paper

You can keep `.svg` or switch to `.jpg`/`.png`; just match the filename in `index.html`.

## Deploy to GitHub Pages
1. Create a repo named **`<your-username>.github.io`** (e.g. `akres001.github.io`).
2. Push these files to the `main` branch:
   ```bash
   cd page
   git init
   git add .
   git commit -m "Initial academic homepage"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source: Deploy from a branch → main / root**.
4. Your site goes live at `https://<your-username>.github.io`.
