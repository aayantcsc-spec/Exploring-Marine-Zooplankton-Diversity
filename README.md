# Eighty years of nets on the Mumbai coast

A synthesis of zooplankton sampling on the Mumbai coast, 1940s–2025.

**Live page:** https://aayantcsc-spec.github.io/Exploring-Marine-Zooplankton-Diversity/

> **Status: working draft.** Quantitative claims in this review were assembled from published abstracts and repository metadata, not from full texts. Every figure needs confirming against the original paper before this is submitted anywhere. See [Outstanding verification](#outstanding-verification).

---

## What this is

Zooplankton has been sampled off Mumbai since the 1940s — across ports, creeks, mangroves, estuaries and open beaches. Those records have never been read together. This repository holds a narrative synthesis that assembles nine sampling efforts spanning roughly eighty years, published as a single self-contained web page.

Three findings come out of reading them side by side:

1. **Copepods dominate every survey**, regardless of decade, habitat or method. This is the only axis on which the studies are genuinely comparable.
2. **Nutrient loading appears to be restructuring the northern estuarine community** away from crustacean plankton, a signal supported independently by falling zooplankton density in Thane Creek monitoring while richness held roughly constant.
3. **Sampling design determines apparent diversity.** One 2022–23 beach survey recorded no meroplankton at all, on a coastline where larval forms contributed 16.75% of estuarine abundance in the same months. Gear, depth and time of day explain the gap, not the water.

The practical conclusion: the Mumbai coast has no comparable zooplankton time series, only a sequence of methodologically incompatible snapshots. The review closes with a proposed minimum reporting protocol.

## What's in this repository

| File | Description |
|---|---|
| `index.html` | The full review as a self-contained page, including an interactive timeline of the sampling record |
| `README.md` | This file |

The page has no build step and no dependencies. CSS and JavaScript are inline. The only external request is a Google Fonts stylesheet, which degrades to Georgia if blocked.

## Running it

Open `index.html` in any browser. That's the whole process.

To host it, GitHub Pages serves it directly — Settings → Pages → deploy from the `main` branch root. The file must be named `index.html` for Pages to serve it at the repository root URL.

## Editing the timeline

The nine studies are a JavaScript array near the bottom of the file:

```js
var studies = [
  { x: 1983, span: "1983", label: "Thal, nearshore waters", flagged: true,
    body: "…", gear: "Nearshore to offshore transect" },
  …
];
```

`x` is the plotting year, `span` the label shown in the detail panel, and `flagged` marks studies that sampled a habitat where larval forms were expected. To add a study, append an object here and one value to the `heights` array immediately below, which staggers the markers so dense clusters stay readable.

Colours are CSS custom properties at the top of the file, with light and dark variants.

## Source data and attribution

**This review is my own work. The dataset it discusses is not.**

The one openly licensed dataset drawn on directly is:

> Ojha S, Yadav R, Barve V (2025). *Exploring Marine Zooplankton Diversity In Mumbai's Coastline, Maharashtra, India.* Occurrence dataset. Published by Thakur College of Science and Commerce, Kandivali East, Mumbai. 59 records, Darwin Core Archive, CC0 1.0.
> GBIF: https://www.gbif.org/dataset/99685588-3922-4ffc-b434-027de443c6fb

The corresponding paper is Ojha, S. & Yadav, R. (2025), *Journal of Advanced Zoology* 46(2), 45–54, [doi:10.53555/jaz.v46i2.5181](https://doi.org/10.53555/jaz.v46i2.5181).

That dataset is CC0, so no permission is needed to reuse it — only correct citation. It appears in this review as one input among nine, and as the worked example in the sampling-design section. All other figures come from the published literature and have not been recomputed from primary data.

All remaining references are listed in full at the end of the page, with unverified entries flagged.

## Outstanding verification

Before this goes to any journal or preprint server:

- [ ] Retrieve full texts for every reference and confirm each quantitative figure
- [ ] Determine whether Takar (2018) and the Sadasivan mangrove study are one work or two
- [ ] Resolve the full citation for the Karanja estuary study
- [ ] Locate the original Gokhale & Athalye (1993) source rather than the second-hand comparison
- [ ] Raise with the original authors: the beach survey's description gives collection commencing 22 September 2022, while its dataset metadata records temporal coverage beginning 22 October 2022
- [ ] If targeting a journal that expects PRISMA, add a documented search strategy, databases queried, inclusion criteria and a flow diagram — this is currently a narrative synthesis, not a systematic review

## Licence

The review text, page design and code in this repository are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — reuse freely with attribution.

The GBIF occurrence dataset discussed here is CC0 1.0 and belongs to its own authors; see the attribution above.


**Aayan Abdul Mannan Shaikh**
M.Sc. Information Technology, Thakur College of Science and Commerce, Kandivali (E), Mumbai 400101, Maharashtra, India

## Citing this

> Shaikh, A.A.M. (2026). *Eighty years of nets on the Mumbai coast: a synthesis of zooplankton sampling, 1940s–2025.* Working draft. https://github.com/aayantcsc-spec/Exploring-Marine-Zooplankton-Diversity
