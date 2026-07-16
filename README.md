# treymcmillon.com — site files

**Design system:** matches the existing Music Week Archive app already
live on your site — white/light-gray cards, coral accent (`#E3836D`),
system sans-serif (Segoe UI). All tokens live in `css/style.css`.

## Folder structure

```
site/
├── index.html              → homepage (project grid)
├── css/style.css           → shared styles, used by every page
├── projects/
│   └── template.html       → copy this for each of the 10 projects
└── music-week/
    └── archive.html        → Music Week archive page
```

## Filling in your projects

1. For each project, copy `projects/template.html` to a new file, e.g.
   `projects/sync-nyc.html` (the homepage already links to these filenames —
   see `index.html` if you rename anything).
2. Open the new file and replace:
   - `<title>` — the browser tab text
   - `<span class="tag">` — "Architecture" or "Graphic Design"
   - `<h1>` — the real project title
   - the description paragraph
   - each placeholder image `<div class="media-placeholder">...</div>`
     with a real `<img>` tag once you have photos (an example is
     commented directly above it in the file)
3. Put your images in a matching folder under `images/`, e.g.
   `images/sync-nyc/render1.jpg`

## Updating the homepage thumbnails

In `index.html`, each project currently shows a text placeholder instead
of a photo:

```html
<div class="project-thumb is-placeholder">Photo goes here — SYNC — NYC</div>
```

Once you have a thumbnail image, replace that div with:

```html
<div class="project-thumb">
  <img src="images/sync-nyc/thumb.jpg" alt="SYNC — NYC">
</div>
```

## Music Week archive

`music-week/archive.html` has 5 friend entries filled in from your
screenshot, plus one stubbed entry (Greg Miller) with placeholder dashes.
Copy the `<article class="record-card">` block to add more friends —
each one needs its own `--tab-color` (any hex works) so the catalog tab
and avatar stay unique per person.

## Deploying

1. Push this whole `site/` folder to a GitHub repo
2. Import the repo into Vercel
3. Once it's live on the `.vercel.app` URL, follow the domain steps we
   went through to point treymcmillon.com at it via Squarespace DNS
