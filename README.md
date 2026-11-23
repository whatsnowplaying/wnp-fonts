# wnp-fonts

Fonts used by the What's Now Playing display templates, hosted here so builds do not depend on
third-party font sites. Only fonts whose licences allow redistribution belong in this repo.

## Layout

Each font has its own directory holding the file the templates load and its licence text:

```text
<name>/<file>.woff2
<name>/OFL.txt or LICENSE.txt
```

## Fonts

| File | Licence | Source |
| --- | --- | --- |
| `bebas-neue.woff2` | SIL OFL 1.1 | Google Fonts, `bebasneue/v16` |
| `canada1500-bd.woff2` | CC0 1.0 | Typodermic Fonts, v1.110 (2025-07 package) |
| `heebo.woff2` | SIL OFL 1.1 | Google Fonts, `heebo/v28` |
| `montserrat.woff2` | SIL OFL 1.1 | Google Fonts, `montserrat/v31` |
| `orbitron.woff2` | SIL OFL 1.1 | Google Fonts, `orbitron/v35` |
| `playfair-display.woff2` | SIL OFL 1.1 | Google Fonts, `playfairdisplay/v40` |
| `rajdhani.woff2` | SIL OFL 1.1 | Google Fonts, `rajdhani/v17` |
| `rubik.woff2` | SIL OFL 1.1 | Google Fonts, `rubik/v31` |

The Google Fonts files are unmodified copies of the Latin subsets served by `fonts.gstatic.com`.
Licence texts come from <https://github.com/google/fonts>.

Canada 1500 Bold is the full font from <https://typodermicfonts.com/canada1500/>, converted from
the package's `canada1500-bd.otf` to WOFF2 with fontTools; the glyphs and character map are unchanged.
It is not subset because WNP users display metadata in many languages.

## Using a font

Builds download each font from this repo by the URL in `vendor.yaml`, pinned to a commit:

```text
https://raw.githubusercontent.com/whatsnowplaying/wnp-fonts/<commit>/rubik/rubik.woff2
```

Pin a commit SHA, never `main`, so a later change here cannot alter what an existing build
downloads. Keep the files in plain git; Git LFS would make these URLs serve pointer files.
