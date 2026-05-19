# Xinyue Wang — Academic Personal Site

A clean, editorial-style academic website built with Jekyll and hosted on GitHub Pages.

---

## Quick Deploy (10 minutes)

### Step 1 — Create the repository

1. Go to <https://github.com/new>
2. Repository **name** must be exactly: `YOUR-USERNAME.github.io`
   (replace `YOUR-USERNAME` with your actual GitHub username, e.g. `xinyuewang.github.io`)
3. Set it to **Public**
4. Do **not** initialize with a README, .gitignore, or license
5. Click **Create repository**

### Step 2 — Upload these files

Easiest path (no command line):

1. On the new empty repo page, click **uploading an existing file**
2. Drag every file and folder from this project into the upload area
3. Commit message: `Initial site`
4. Click **Commit changes**

Or via terminal:

```bash
cd path/to/this/folder
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. In your repo, go to **Settings** → **Pages** (left sidebar)
2. Under "Build and deployment":
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` / `/ (root)`
3. Click **Save**
4. Wait 1–2 minutes, then visit `https://YOUR-USERNAME.github.io`

### Step 4 — Add your real photo and CV

Two files to replace (delete the `README.txt` files in each folder):

- `assets/img/profile.jpg` — your portrait (vertical orientation works best, ~600×750px)
- `assets/cv/Xinyue_Wang_CV.pdf` — your CV PDF

You can do this directly on GitHub (click the folder → **Add file → Upload files**).

### Step 5 — Update site URL

Open `_config.yml` and change line:

```yaml
url: "https://YOUR-GITHUB-USERNAME.github.io"
```

to your real URL. Commit. GitHub Pages will rebuild automatically (~1 min).

---

## File Structure

```
├── _config.yml          # Site settings & navigation
├── _layouts/
│   └── default.html     # Master HTML template
├── _includes/
│   ├── head.html        # <head> contents (fonts, meta)
│   ├── header.html      # Top navigation bar
│   └── footer.html      # Footer
├── assets/
│   ├── css/style.css    # All visual styling
│   ├── img/profile.jpg  # YOUR PHOTO (replace)
│   └── cv/*.pdf         # YOUR CV (replace)
├── index.md             # About page (landing)
├── research.md          # Research & papers
├── teaching.md          # Teaching (optional)
├── cv.md                # CV summary page
└── README.md            # This file
```

## How to Edit Content

- **About page text:** edit `index.md`
- **Add a paper:** open `research.md`, copy one of the `<li class="paper">…</li>` blocks
- **Change navigation:** edit the `nav:` section in `_config.yml`
- **Remove Teaching page:** delete `teaching.md` and remove the Teaching entry from `_config.yml`
- **Change colors:** edit the `:root` CSS variables at the top of `assets/css/style.css`
  - `--accent` is the deep teal — change to any hex color you like
  - `--paper` is the warm background — `#FFFFFF` for pure white, `#FAF7F2` for warm paper

## Local Preview (optional)

If you have Ruby installed, you can preview locally before pushing:

```bash
gem install bundler jekyll
bundle init
echo 'gem "jekyll"' >> Gemfile
bundle install
bundle exec jekyll serve
```

Then visit <http://localhost:4000>.

## Custom Domain (optional, later)

If you buy a domain (e.g. `xinyuewang.com`):

1. Add a file named `CNAME` to the repo root, containing only your domain
2. In Settings → Pages, enter the custom domain
3. Configure DNS at your registrar to point to GitHub Pages

---

## Design Notes

- **Display font:** Fraunces (a contemporary editorial serif)
- **Body font:** Source Serif 4 (designed for long-form reading)
- **UI font:** Inter Tight (used only for nav, labels, buttons)
- **Palette:** warm paper background, deep ink text, dark teal accent
- **No JavaScript required** — the site is pure HTML/CSS, fast and accessible
