# Yinan Li's academic website

A single-page academic homepage made with plain HTML and CSS. No JavaScript, build step, or package installation is required. Lato loads through the optional Google Fonts stylesheet; system fonts are used if it is unavailable.

## Files

- `index.html`: introduction, contact links, and seven publications.
- `style.css`: typography, colors, spacing, responsive layout, and print styles.
- `assets/profile.jpg`: website portrait.
- `assets/YinanLi_CV.pdf`: downloadable CV.
- `.nojekyll`: tells GitHub Pages to serve the files directly.

The original photo and PDF in the project root are preserved as supplied. The website uses the copies in `assets/`.

## Preview locally

From this folder, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000 in your browser. Stop the server with Ctrl+C. You can also open `index.html` directly.

## Update content

### About text and links

Edit the paragraphs inside `.about-text` in `index.html`. The job-market announcement is the paragraph with `class="job-market"`. Contact links are in `.contact-links`; the header navigation is in `.site-header`.

### Add or edit a publication

Inside `<ol class="publication-list">`, copy one complete `<li>…</li>` entry and edit its title, full author list, venue/year, and paper URL. Update the paper link's `aria-label` as well. Put `<strong>Yinan Li</strong>` around your name. For equal contributions, use `<sup>*</sup>` and retain the explanatory note. Entries appear in their HTML order.

### Replace the CV

Replace `assets/YinanLi_CV.pdf` with the new PDF, retaining the filename. Both CV links use this path and open the PDF in a new tab.

### Replace the photograph

Replace `assets/profile.jpg` with your new photograph. If its dimensions change, update the image's HTML `width` and `height` attributes to its actual pixel dimensions; CSS controls its display width and preserves its natural aspect ratio. If you use a different filename or format, update `src` as well. No image generation or cropping is needed.

## GitHub Pages

Repository: [yinan11a/yinan11a.github.io](https://github.com/yinan11a/yinan11a.github.io).

Website address: [https://yinan11a.github.io/](https://yinan11a.github.io/).

The publishing source is the `main` branch, repository root. The setup instructions below are retained for reference.

For the personal homepage at `https://yinan11a.github.io/`:

1. Sign in to GitHub as `yinan11a` and create a public repository named `yinan11a.github.io`. If this repository already exists, inspect and back up its contents before replacing an existing site.
2. Upload `index.html`, `style.css`, `.nojekyll`, and the `assets/` folder to the repository root. You may include this README; the original root-level CV and photo do not need to be uploaded.
3. In the repository's **Settings → Pages**, select **Deploy from a branch**, then select the **main** branch and **/ (root)** folder, and save.
4. Wait for GitHub's Pages deployment to complete, then visit the URL shown in those settings.

If you prefer a repository with a different name, the default URL is `https://yinan11a.github.io/REPOSITORY-NAME/`. All local asset links are relative, so this layout works there too.

To update a published site, commit or upload your edited files to the publishing branch. GitHub Pages redeploys them automatically. Check the deployment status in GitHub if your changes do not appear immediately, then refresh the browser.

Nothing is published by running the local preview. Local edits must be uploaded or committed to the GitHub repository to update the public site. This workspace is a plain folder; to use Git locally, clone the repository into a separate folder.

Reference: [GitHub's guide to creating a Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).
