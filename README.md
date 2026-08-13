# Sustainable Mobility & Logistics Lab — Website

Website for Dr. Lakshay's lab, Department of Mechanical Engineering, IIT (BHU) Varanasi.
Plain HTML/CSS — no build step, no paid hosting. Deployed free with **GitHub Pages**.

## File structure

```
sml-lab/
├── index.html          → Home / About page
├── research.html        → Research areas
├── people.html           → PI, PhD/M.Tech scholars, collaborators, "join us"
├── publications.html   → Journal + conference papers
├── projects.html        → Funded grants + agency engagements
├── contact.html         → Contact details + embedded map
├── css/
│   └── style.css        → All styling (single shared stylesheet)
└── assets/
    ├── photos/           → Put people's photos here (see below)
    └── icons/            → Optional icons/logo files
```

## 1. How to publish this for free on GitHub Pages

1. Create a **new public GitHub repository**, e.g. `sml-lab` (or `<your-username>.github.io` if you want it as your main GitHub Pages site).
2. Upload all files in this folder to that repository (keep the folder structure — `css/` and `assets/` must stay as subfolders).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source: Deploy from a branch**, **Branch: main**, folder **/(root)**. Save.
5. After a minute, your site will be live at:
   - `https://<your-username>.github.io/sml-lab/` (if repo is named `sml-lab`), or
   - `https://<your-username>.github.io/` (if the repo is named exactly `<your-username>.github.io`)

No payment, no server, no domain required. GitHub Pages is free forever for public repositories.

**Optional — custom domain:** if the lab later buys a domain (e.g. `smllab.in`), add a `CNAME` file with the domain name at the repo root and point the domain's DNS to GitHub Pages. Entirely optional — the free `github.io` URL works fine on its own.

## 2. Adding real photos (currently placeholders)

Right now, the PI and each student show a circular avatar with initials (e.g. "DL") instead of a photo. To swap in a real photo:

1. Save the photo as a square image (min. 300×300px) into `assets/photos/`, e.g. `assets/photos/lakshay.jpg`.
2. In the relevant HTML file, find the block like:
   ```html
   <div class="avatar">DL</div>
   ```
   and replace it with:
   ```html
   <div class="avatar"><img src="assets/photos/lakshay.jpg" alt="Dr. Lakshay"></div>
   ```
3. Repeat for each student in `people.html`.

## 3. Adding a logo

Currently the header shows a circular "SML" text mark instead of a logo. To replace it with a real logo:

1. Save your logo file into `assets/icons/logo.png` (transparent background recommended).
2. In every HTML file's header, replace:
   ```html
   <div class="brand-mark">SML</div>
   ```
   with:
   ```html
   <div class="brand-mark"><img src="assets/icons/logo.png" alt="Lab logo" style="width:100%;height:100%;object-fit:contain;border-radius:50%;"></div>
   ```

## 4. Updating content

- **Announcements / open positions**: edit the `.announce` block in `index.html` and `people.html`.
- **Adding a new publication**: copy an existing `<div class="pub">...</div>` block in `publications.html` and edit the text — group under the right `<div class="pub-year">YYYY</div>` heading.
- **Adding a new student**: copy an existing `.card.person` block in `people.html`.
- **Adding a new project**: copy a `.stop` block in `projects.html`.
- **Colors/fonts**: all defined once at the top of `css/style.css` under `:root { ... }` — change a hex value there and it updates across every page.

## 5. Checking it locally before publishing

You don't need any software installed — just double-click `index.html` and it opens in your browser. Click through the nav to check all pages before uploading to GitHub.

## 6. Renaming the lab

If you want a different lab name than "Sustainable Mobility & Logistics Lab":
- Use "Find and Replace" across all `.html` files for the phrase `Sustainable Mobility &amp; Logistics Lab` (and `SML` for the short mark).
- Also update the `<title>` tag at the top of each file.

## Content sources

All research, project, funding, and student information was compiled from Dr. Lakshay's official IIT (BHU) faculty page and public Google Scholar profile as of August 2026. Please review and correct any details (exact grant amounts, publication venues/DOIs, student names) before publishing — placeholders marked "Update with exact venue & DOI" in `publications.html` still need to be filled in with real citation details.
