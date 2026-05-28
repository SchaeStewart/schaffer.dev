# schaffer.dev

Landing page for **Schaffer Dev LLC** — served at https://schaffer.dev via GitHub Pages.

## Stack

Vanilla HTML, CSS, and a one-line JS file. No build step, no dependencies.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Single-page markup with hero, contact links, footer |
| `styles.css` | All styling; auto light/dark via `prefers-color-scheme` |
| `script.js` | Sets the footer year |
| `CNAME` | Pins the Pages site to the apex domain `schaffer.dev` |
| `.nojekyll` | Disables Jekyll so files publish as-is |

## Local preview

Open `index.html` directly in a browser, or serve the directory:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Any push to `main` is published by GitHub Pages. There is no build step.

## DNS

At the registrar, point `schaffer.dev` at GitHub Pages:

- Apex `A` records:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- Optional `www` `CNAME` → `schaestewart.github.io`

After DNS propagates, enable **Enforce HTTPS** in repo Settings → Pages (or
re-run the Pages API `PUT` with `https_enforced=true`).
