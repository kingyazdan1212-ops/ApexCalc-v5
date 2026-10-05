# ApexCalc v6.0 — Final Release

A calculator-only PWA with dedicated in-app keyboards for every workspace.

## What was hardened in v6
- Phone keyboard suppression for keypad-only fields (`readonly`, `inputmode=none`, focus/touch guards).
- Tap-noise / double-trigger guard to prevent accidental duplicate button actions on touch devices.
- Reduced visual compositing artifacts with isolated/contained panels and GPU-stable layers.
- Reduced-motion support and cleaner touch feedback.
- Input length limits and defensive local-history loading.
- Safer localStorage handling when storage is blocked or corrupted.
- Graph redraw token guard to prevent stale renders during rapid interaction.
- Graph range status is synchronized with the actual zoom value.
- Duplicate element IDs checked during release QA.
- JavaScript syntax checked with Node.js.
- Responsive mobile-first layout retained.
- Dedicated keyboards retained for Calculator, CAS, Graph, Equations, Matrix, Statistics, Base-N and Converter.

## Included
- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icon.svg`

## Publish
Upload the contents of this folder to a GitHub repository and enable GitHub Pages.

## APK note
The app is PWA-ready. The math engine is currently loaded from the math.js CDN, so a fully offline APK build should bundle math.js locally before packaging.

## Release QA
- HTML structure inspected
- Duplicate IDs: none detected
- JavaScript syntax: passed
- Dedicated keypad fields: guarded
- Touch duplicate-action protection: enabled
- Graph stale-render protection: enabled
- Local history failure protection: enabled
