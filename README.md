# Shivam Roy — Portfolio Site

A single self-contained file: `index.html`. No build step, no dependencies to install.

## Files in this project

- `index.html` — the site
- `profile.jpg` — your headshot, referenced by the hero section. Keep it in the same folder as
  `index.html` (same name, or update the `src="profile.jpg"` in the `<img>` tag if you rename it).
- `README.md` — this file

## Editing your content

Everything lives in `index.html`. Open it in any text editor (VS Code recommended).

- **Hide something** (a job, a project, a certification): find its block and add the word `hidden` to
  its opening tag, e.g. `<article class="card" hidden>`. It stays in the file, just doesn't render.
- **Show something you've hidden**: delete the word `hidden` from that tag.
- **Add a new project / certification / job**: copy one of the existing blocks (search for the HTML
  comments like `<!-- Example hidden project card -->`) and edit the text and links.
- **Project links**: each project card has a GitHub icon linking to `github.com/shivamRoy04` — point it
  at the specific repo instead of your profile. Search the file for `LIVE_URL_PLACEHOLDER` to find the
  Traveller's Hub live-demo link and swap the `#` for your actual Render URL.
- **Reorder projects**: display order is just the order the `<article class="proj-card">` blocks appear
  in the file — cut and paste a whole block to move it earlier or later.
- **Add a project**: copy the hidden template card at the bottom of the Projects section (it already has
  a metrics row and a "What's next" roadmap list stubbed in), remove `hidden`, and fill it in.
- **Resume download button**: the hero's "Download resume" button links to `/resume.pdf`. Add a file
  named `resume.pdf` next to `index.html` and it'll work as-is.
- **Colors/fonts**: all defined once at the top of the `<style>` block under `:root { ... }` — change a
  hex value there and it updates everywhere.

## Hosting it for free

Any of these work well for a static single-file site. GitHub Pages is the most common for a dev portfolio
since it doubles as proof you use Git.

### Option A — GitHub Pages (recommended)
1. Create a new **public** GitHub repo, e.g. `shivamRoy04/portfolio` (or `shivamRoy04.github.io` for a
   root-level URL — see note below).
2. Upload `index.html`, `profile.jpg`, and `resume.pdf` (if you have one) to the repo — either via
   the GitHub web UI ("Add file → Upload files") or:
   ```bash
   git init
   git add index.html profile.jpg resume.pdf
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/shivamRoy04/portfolio.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
5. Save. After a minute your site is live at:
   - `https://shivamRoy04.github.io/portfolio/` (repo named anything), or
   - `https://shivamRoy04.github.io/` (only if you name the repo exactly `shivamRoy04.github.io`).

### Option B — Netlify
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the whole folder (containing `index.html` and `profile.jpg`) onto the page — not just the
   HTML file, or your photo won't load.
3. Netlify gives you a live URL instantly (e.g. `random-name-123.netlify.app`); you can rename it for
   free in **Site settings → Change site name**.
4. Optional: connect it to a GitHub repo later for auto-deploys on every push.

### Option C — Vercel
1. Push the folder to a GitHub repo (same as Option A, steps 1–2).
2. Go to [vercel.com/new](https://vercel.com/new), import the repo, leave settings as default (no
   framework/build command needed for a plain HTML file), and deploy.
3. You get a `your-project.vercel.app` URL, with automatic redeploys on every push.

### Custom domain (optional, still free-ish)
All three options let you attach a custom domain for free — you'd only pay for the domain itself
(~₹700–1000/yr from providers like Namecheap or Porkbun). Point the domain's DNS at GitHub
Pages/Netlify/Vercel per their docs, and HTTPS is issued automatically.

## After deploying
Update the `mailto:`, GitHub, and LinkedIn links in `index.html` if any of them change, and swap the
placeholder project "live demo" link once something is hosted on Render.
