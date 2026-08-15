# Kaen Kogashi — GitHub Pages template

A lightweight one-page academic portfolio inspired by the overall information architecture of
`hhd000exe.github.io`, with a custom green visual design.

## Files

- `index.html` — main page
- `style.css` — all styling
- `assets/profile-placeholder.svg` — replace with your portrait
- `assets/mmhoi-placeholder.svg` — replace with a paper/project teaser
- `assets/Kaen_Kogashi_CV.pdf` — add your CV using exactly this filename, or update the link in `index.html`

## Before publishing

Search `index.html` for these placeholders and replace them:

1. `YOUR_EMAIL@example.com`
2. `https://scholar.google.com/`
3. `https://www.linkedin.com/`
4. The generic arXiv link `https://arxiv.org/`
5. The `Project Page` link (`href="#"`)
6. Profile photo and MMHOI teaser images
7. Any biography / affiliation wording you want to adjust

## Publish as https://kaenkogashi.github.io/

### Browser-only method

1. Sign in to GitHub.
2. Click **New repository**.
3. Repository name MUST be exactly: `kaenkogashi.github.io`
4. Choose **Public**.
5. Create the repository.
6. Click **Add file → Upload files**.
7. Upload `index.html`, `style.css`, and the entire `assets` folder.
8. Commit the files to the `main` branch.
9. Open **Settings → Pages**.
10. Under **Build and deployment**, choose:
    - Source: **Deploy from a branch**
    - Branch: **main**
    - Folder: **/(root)**
11. Save.
12. Open `https://kaenkogashi.github.io/`.

### Git command method

```bash
git clone https://github.com/kaenkogashi/kaenkogashi.github.io.git
cd kaenkogashi.github.io

# Copy index.html, style.css and assets/ into this folder.

git add .
git commit -m "Create academic homepage"
git push origin main
```

Then enable GitHub Pages from **Settings → Pages** if it is not already enabled.

## Replace the portrait

Put your image at:

`assets/profile.jpg`

Then change this line in `index.html`:

```html
<img src="assets/profile-placeholder.svg" ... />
```

to:

```html
<img src="assets/profile.jpg" ... />
```

A portrait with a 4:5 aspect ratio works best.

## Replace the MMHOI teaser

Put a teaser image at:

`assets/mmhoi.jpg`

and change:

```html
<img src="assets/mmhoi-placeholder.svg" ... />
```

to:

```html
<img src="assets/mmhoi.jpg" ... />
```


## Videos

The reference site hosts MP4 files directly on GitHub Pages. You can use the same approach.

1. Put `assets/MMHOI-demo.mp4` in the repository.
2. Link to it:
```html
<a href="assets/MMHOI-demo.mp4" target="_blank">Video</a>
```
3. Or embed it:
```html
<video controls playsinline preload="metadata" poster="assets/MMHOI.png">
  <source src="assets/MMHOI-demo.mp4" type="video/mp4">
</video>
```

H.264 video + AAC audio in MP4 is the safest choice for browser compatibility.


## MMHOI video gallery

The MMHOI publication card is configured for up to three MP4 videos:

- `assets/1.mp4`
- `assets/2.mp4`
- `assets/3.mp4`

Replace the zero-byte placeholder files with your real MP4 files, keeping the same filenames.
For broad browser compatibility, encode as H.264 video in an MP4 container (AAC audio if needed).
If you use fewer than three videos, remove the corresponding `<video>...</video>` block from `index.html`.
