# /line-angle

**Straight-line angles** — a self-contained HTML animation that teaches what a straight
line measures, how to name acute/obtuse angles, and how to work out a missing angle
(180 − 60 = 120°) with two multiple-choice questions and a subtraction puzzle.

Live URL: <https://akhadir.github.io/line-angle/>

## Hosting model

This folder lives in the `akhadir.github.io` repository, which is used as a common host
for standalone pages. The rule is simply:

> **one sub-folder per project, containing an `index.html`**

so `line-angle/index.html` is served at `/line-angle/`. To publish another project, add a
folder with an `index.html` in it and the URL follows the same shape.

Two properties make this safe for files added directly to this repo:

- `.nojekyll` is present, so Pages serves every file as plain static content with no
  Jekyll processing or front-matter requirement.
- The `sync_changes.yml` workflow pulls from `flatmaintenance` with
  `rsync -av --exclude='.git/'` — note there is **no `--delete`**, so folders that exist
  only here are left untouched by a sync.

## The page itself

- One file, no build step, no dependencies, no network access, no external fonts or
  scripts — it runs offline straight from the filesystem.
- All artwork is inline SVG. The only `<defs>` block is shared across the six scenes.
- No `<script src>`, `<img>`, `<link>`, `innerHTML`, or `http(s)://` references, so it
  will keep working from any path on any host.
