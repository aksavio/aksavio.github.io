# aksavio.github.io

Personal site of Akash Savio Sen, published with GitHub Pages at
<https://aksavio.github.io>.

It is a plain, hand-written static site — no build step, no framework. The
repository root is the web root, so `index.html` is the home page and every page
is served from the path where it lives.

## Layout

```
.
├── index.html            # home page (served at /)
├── work.html             # project index
├── resume.html
├── ...                   # one HTML file per page, all at the repo root
├── Alpha_Module/         # self-contained project (page + its images)
│   └── ModuleAlpha.html
└── assets/
    ├── css/              # site.css, carousel.css, new.css, style.css, voodoo.css, coda.css
    ├── images/           # images shared by several pages
    ├── media/            # loose gifs / videos used by project pages
    ├── andaman/ dap/ moto/ pings/ poster/ star/ visual-book/ voodoo/
    └── ...
```

Page URLs are intentionally kept stable (e.g. `/Voodoo.html`,
`/lightmeter.html`), so do **not** move or rename a page file without also
updating every link to it — including the absolute
`https://aksavio.github.io/...` links used inside some pages.

## Editing

- Keep asset references relative to the repo root, using forward slashes
  (e.g. `assets/images/egg.webp`).
- Shared CSS lives in `assets/css/`:
  - `site.css` — the simple monospace theme (`#main`) used by the plain pages.
  - `carousel.css` — the slideshow used by `andaman`, `book`, `gallery`,
    `posters` and `star`.
  - `new.css` — Typora export theme used by the write-up pages.
  - `style.css` — older theme used by `audio`, `test` and `exploring_delhi`.
  - `voodoo.css` + `coda.css` — used by `Voodoo.html`.

## Preview locally

Because everything is static, any static server works:

```sh
python3 -m http.server 8000
# then open http://localhost:8000/
```
