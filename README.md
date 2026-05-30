# VWP Stimulus Catalog

A community-maintained index of openly available **stimulus sets and study repositories for the Visual World Paradigm (VWP)**.

**Live catalog:** https://vocaliodmiku.github.io/vwp-catalog/

## What this is

The VWP is widely used in psycholinguistics, but its stimuli are scattered: some live in general object/image banks (e.g. BOSS), most live in per-study OSF repositories tied to one experiment's design, and the controlled *linguistic* materials (cohort/rhyme/semantic competitor sets) usually have to be reconstructed from papers' methods sections. There is no single place to see what exists.

This catalog is that place. It is a structured, searchable index.

## What this is **not**

- **It hosts nothing.** Every entry links out to the original source. No stimuli, audio, or data are redistributed here.
- **It does not grant any license.** Each source carries its own terms — *always check the `license` field and the source itself before reuse.* An entry's presence here is not permission to use it.
- **Scope is VWP-specific.** General eye-tracking or scene-perception stimulus banks are included only when they are a common source for building VWP displays (e.g. BOSS).

## How it works

All data lives in a single file: [`catalog.csv`](catalog.csv). The web page (`index.html`) renders directly from it — so the catalog is simultaneously human-browsable (filter/sort/search in the browser) and machine-readable (grab the CSV directly, or point a future script/package at it).

### Schema

| field | meaning |
|---|---|
| `id` | short unique slug |
| `name` | display name of the set |
| `citation` | full reference |
| `year` | publication year |
| `competitor_type` | cohort / rhyme / semantic / anticipatory / none / methodological, etc. |
| `language` | language of linguistic materials (or "language-independent") |
| `stimulus_modality` | line drawings / object photos / clipart scenes / real objects |
| `audio_included` | yes / no / unknown |
| `eyetracking_data_included` | yes / no / unknown — whether human fixation data is shared |
| `n_items` | number of items, if known |
| `license` | license of the **source** (or "unclear") |
| `source_url` | link to the original source |
| `notes` | caveats, design details, usability notes |

## Contributing

Add or correct an entry by editing [`catalog.csv`](catalog.csv) and opening a pull request, or open a [New stimulus set issue](../../issues/new/choose) and a maintainer will add it. One row per set. Keep `license` honest — use `unclear` rather than guessing.

## License

The catalog **content** (the `catalog.csv` metadata and site code) is released under CC0 / MIT (see `LICENSE`). This applies only to this index — **not** to any linked stimuli, which retain their own licenses.
