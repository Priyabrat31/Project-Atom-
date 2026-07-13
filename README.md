# ପାଞ୍ଚଟି ସୁରକ୍ଷା କବାଟ (Five Security Doors)

An Odia-language browser escape-room / mystery game. The player solves
five puzzle "doors" (stages) to uncover what happened to a missing
scientist.

## Structure

```
.
├── index.html              Home screen, intro cutscene + story text
├── stage1.html              Stage 1 puzzle
├── stage2.html              Stage 2 puzzle
├── stage3.html              Stage 3 puzzle
├── stage4.html              Stage 4 puzzle
├── stage5.html              Stage 5 puzzle
├── ending.html               Ending screen
├── assets/
│   └── img/                  Favicon and any other images
├── .nojekyll                  Tells GitHub Pages not to run Jekyll processing
└── .gitignore
```

Flow: `index.html → stage1.html → stage2.html → stage3.html → stage4.html → stage5.html → ending.html → index.html`

## Running locally

No build step or server-side code — just open `index.html` in a
browser, or serve the folder with any static file server, e.g.:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `project-atom`).
2. From inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial deployable version"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source** →
   select **Deploy from a branch**, branch **main**, folder **/(root)**
   → **Save**.
4. Wait 1-2 minutes, then your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

Because `index.html` sits at the repository root, GitHub Pages will
serve it automatically as the site's home page — no extra
configuration needed.

