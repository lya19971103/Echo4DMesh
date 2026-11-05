# Echo4DMesh

Research demonstrations of patient-specific cardiac reconstruction.

## Interactive demo gallery

The static website is in [`docs/index.html`](docs/index.html). It includes:

1. Normal, HCM and MI LV/epicardial motion animations.
2. Held-out A2C mask comparisons before and after shape adaptation.
3. Three-view LV cross-sectional overlap through a cardiac cycle.
4. Two whole-heart motion examples.
5. Rotating static end-diastolic LV reconstructions with CT references.
6. Cine MRI mesh overlays synchronized with normalized volume curves.

Open `docs/index.html` locally (no build, dependencies, server or external fonts required). Animations start on demand. MRI players support pause and per-frame scrubbing. On mobile, panels stack vertically.

For GitHub Pages, choose **Settings → Pages → Deploy from a branch → main → /docs**. The expected URL after successful deployment is `https://lya19971103.github.io/Echo4DMesh/`; this is not a claim that hosting has already been enabled.

## Interpretation and provenance

- Public assets use display aliases. Raw ultrasound, CT/MRI scans, original subject identifiers, acquisition dates, and local source paths are not included.
- Clinical motion assets are derived from stored LV trajectories with fitted epicardial sidecars. They do not establish true tissue-point tracking or wall-thickness accuracy.
- Held-out A2C masks are excluded from shape encoding/adaptation, but used for probe-pose calibration. This is not a completely untouched target-view test.
- Observed-view overlap measures agreement with input masks, not independent 3D accuracy.
- CT animations rotate a static ED model; they are not temporal CT acquisitions. The paired surfaces use global similarity alignment, including uniform scale. The selected revised-label visualization cases are complementary comparisons, not additional independent validation.
- MRI panels reuse the two selected paper examples and their stored volume curves. All 25 native frames are retained. The curve's 100% endpoint repeats frame 0 for periodic display closure; native frame 24 is 96%. MRI-derived approximate input slices are not clinical echo acquisitions.
- Playback rate is illustrative, not measured heart rate. The gallery is for research communication, not clinical use.

No redistribution license for underlying clinical datasets is granted by this repository. Only derived presentation assets are included.
