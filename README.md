# american-bloodline

**An American Bloodline** — a free family history project. Eighteen generations of
names, records, and stories, kept together so the next generation can find them.

Live site: **https://rickbrew13.github.io/american-bloodline/**

---

## What is in this repository

| Path | What it is |
|------|------------|
| `index.html` | The homepage — hero, About, the two Facebook cards, the Generations section, Surnames, Contribute, footer |
| `styles.css` | All styling for the homepage |
| `images/hero.jpg` | The cover artwork, shown whole and uncropped at the top of the page |
| `images/link-facebook-page.svg` | Banner for the "Follow Our Facebook Page" card |
| `images/link-facebook-group.svg` | Banner for the "Join Our Facebook Group" card |
| `generation-5-hark/` … `generation-18/` | One folder per public generation, each with its own index page |
| `<person-name>/` | One folder per individual profile |

Generations **I–IV** are not in this repository — they are held as private Google
Docs, linked from the homepage, and shared only with family who have been given
access.

---

## The homepage

The homepage is a single static page. It needs no build step, no server, and no
dependencies — open `index.html` in a browser and it works.

**Page order:** Hero → About this project → Two ways into the story (Facebook page
and group) → Generations → Surnames → Contribute → Footer.

**The Generations section** is split into two groups, each introduced by a dark
gold-framed panel that sits between the group heading and the generation cards:

- **Generations I–IV** — "Before you go further" / *The youngest generations*.
  The kids and the parents' generation, held as private documents. 221 people.
- **Generations V–XVIII** — "Open to the public" / *The older generations*.
  Each has its own index page. 1,502 people.

Both panels are plain `<div>` elements with **no links** — the generation cards
underneath are the only way in. Total documented: **1,723 people**.

---

## Editing the homepage

Everything is plain HTML and CSS — no framework, no build.

- **Colours and fonts** are CSS custom properties at the top of `styles.css`
  (`--ink`, `--parchment`, `--gold`, `--brown`, and the three font stacks).
- **A generation card** is one `<a class="gen">` block inside `.gen-grid`. Copy an
  existing one and change the numeral, the name, the count, and the `href`.
- **A group panel** is one `<div class="gen-note">` block. Its eyebrow, heading and
  body text are plain markup.
- **The two Facebook cards** are `<a class="door">` blocks; their banner images are
  the two SVGs in `images/`.

---

## Publishing

This repository is served by **GitHub Pages** from the `main` branch, root folder.

To publish a change: commit and push to `main`. The site rebuilds automatically,
usually within a minute.

**Pages settings** (only needed once): *Settings → Pages → Source: Deploy from a
branch → Branch: `main` / `(root)`*.

The `.nojekyll` file at the root tells GitHub Pages to serve the files as-is
without running Jekyll — leave it in place.

---

## Notes

- The homepage links to the Google Sites index for the full generation index, and
  to Google Docs for Generations I–IV.
- Individual profiles are private and are not linked from the public generation
  index pages.
