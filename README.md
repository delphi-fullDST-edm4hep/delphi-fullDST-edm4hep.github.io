# delphi-fullDST-edm4hep.github.io

The organisation's homepage: <https://delphi-fulldst-edm4hep.github.io/>

A single static `index.html` introducing the three public projects — the simulation pipeline, the
EDM4hep converter and the event display — and linking to each repository and its documentation.
There is no build step; GitHub Pages serves this repository's root directly.

Two pieces are embedded live rather than screenshotted, both same-origin so they need no CORS:

* the **event display**, as the published 3-D figure JSON rendered with plotly.js
  (`delphi-edm4hep-eventdisplay/events/data_48758_2666.3d.json`)
* the **collection map**, in an `<iframe>` of the converter's own page

Both load only when scrolled into view — plotly.js is several MB and most visitors will scroll past.
Because they point at the published artefacts, they stay current on their own: regenerating the
showcase event or rebuilding the collection map updates this page with no edit here.

The project sites keep their own subpaths and are unaffected:

| | |
|---|---|
| `/` | this page |
| `/delphi-edm4hep/` | converter documentation |
| `/delphi-edm4hep-eventdisplay/` | the event display and its manual |

The chain figure is hand-authored inline SVG — no library, no image file. It is themed with
`currentColor` and the page's `--green` variable, so it follows light and dark mode with the rest
of the page, and carries `role="img"` with an `aria-label` stating the same claim as the caption.

When a project is added or renamed, update `index.html` here and the organisation profile in
[`.github/profile/README.md`](https://github.com/delphi-fullDST-edm4hep/.github/blob/main/profile/README.md);
they carry the same copy.
