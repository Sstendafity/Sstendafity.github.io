# sstendafity.github.io

Personal portfolio site. Single static page, no build step, no dependencies.

| File | Purpose |
|---|---|
| `index.html` | The whole site: markup, styles and one small script, all inline |
| `hijab-chat.png` | Screenshot evidence for the Hijab Amira build |
| `og-image.png` | 1200x630 social preview card |
| `robots.txt` / `sitemap.xml` | Search indexing |
| `.nojekyll` | Serve files as-is; skip GitHub's Jekyll build |

Edit `index.html` and push. GitHub Pages redeploys automatically.

## Notes for future edits

The page loads exactly one external resource: IBM Plex Sans and Mono from Google Fonts.
Everything else is inline. The only JavaScript is the theme control: a two-line script in `<head>` that applies a
saved theme before first paint, and the toggle itself at the end of `<body>`. With nothing
saved the page follows `prefers-color-scheme`.

The hero panel is 81 hardcoded `<i>` cells, one per case in the Hijab Amira evaluation
suite, grouped 58 answered / 15 refused / 8 escalated. If those counts change, regenerate
the block rather than editing cells by hand. State is encoded by fill and not by hue, so
the grid still reads without color.
