# Embedded typeface

[JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) v2.304, subset to
only the characters used by the stats graphic, and inlined into `stats.svg` as
base64 `@font-face`.

Why inline it:

* **An external font URL cannot work here.** The SVG is loaded through
  `<img>`, and a browser refuses to fetch subresources for an image document.
  A base64 data URI is the only mechanism, and it keeps the page free of
  third-party requests.

| file | weight | covers |
|---|---|---|
| `jbmono-400.woff2` | 400 | basic latin, for stats.svg |
| `jbmono-600.woff2` | 600 | basic latin, for stats.svg |

Licensed under the SIL Open Font License 1.1 — see `OFL.txt`. Subsetting and
redistribution in this form are permitted; the reserved font name is unchanged.
