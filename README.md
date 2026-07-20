# Caden Ice — Personal Site

A small, hand-built personal website. Single static HTML file, no framework and no build step — just `index.html`, the fonts (loaded from Google Fonts), and the assets folder.

**Live:** _add your GitHub Pages / custom domain URL here once deployed_

## Structure

```
.
├── index.html              # the entire site (markup + content + JS)
├── assets/
│   └── CadenIce-Resume.pdf  # linked from the Professional page
├── .nojekyll               # tells GitHub Pages to serve files as-is
├── .gitignore              # keeps private source notes out of the repo
└── README.md
```

The site has five sections, switched client-side (no page reloads) and deep-linkable via the URL hash: `#home`, `#hobbies`, `#pro`, `#growth`, `#projects`.

## Editing content

All page content lives in plain JavaScript arrays near the top of the `<script>` block in `index.html` — `moments`, `garage`, `experience`, `education`, `certs`, `skillGroups`, `outcomes`, `currently`, `mediaLog`, `projects`, etc. Edit the text there and refresh; no build required.

## Adding photos

Several spots show a striped placeholder with a filename hint (e.g. `assets/portrait.jpg`, `assets/sti.jpg`, `assets/almura.jpg`). To use a real image, drop the file into `assets/` and replace the placeholder `<div>` (or the project's shot `<div>`) with an `<img>` that fills the same box, for example:

```html
<img src="assets/portrait.jpg" alt="Caden Ice"
     style="width:100%; height:100%; object-fit:cover; border-radius:4px;">
```

Filenames the layout currently hints at: `portrait.jpg`, `sti.jpg`, `almura.jpg`, `ridesafe.jpg`, `vault.jpg`.

## Deploying to GitHub Pages

1. Create a new GitHub repository and push this folder.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick your `main` branch and the `/ (root)` folder, and save.
4. Your site will be live at `https://<username>.github.io/<repo>/` within a minute or two.

To use a custom domain, add it under Settings → Pages and create a `CNAME` file with the domain.

## Note on privacy

`content/` (which includes a detailed personal notes file) and the raw Claude Design export are excluded from the repo via `.gitignore`. Keep them local — they were the source material, not part of the published site.
