# VAIDYANATHAM HERBALS — GitHub Website Project

## Upload this complete folder to one GitHub repository

Keep the folder structure and relative paths unchanged. GitHub Pages can publish the repository root directly.

## File groups

```text
vaidyanatham-github-project/
├── index.html                         # Main website entry point
├── README.md                          # This guide
├── css/
│   ├── main.css                       # Complete master CSS; all original style blocks kept in cascade order
│   ├── loading.css                    # Loading-screen styles, extracted for focused editing
│   ├── relax-button.css               # Relax button styles
│   ├── floating-buttons.css           # Floating and quick-action button styles
│   ├── navigation.css                 # Navigation and menu styles
│   ├── consultation.css                # Consultation section styles
│   ├── responsive.css                  # Responsive and final layout styles
│   ├── maps-and-qr.css                 # Map and QR-related styles
│   └── final-overrides.css             # Final polish / override styles
├── js/
│   ├── loading.js                     # Independent loading-screen controller and failsafe
│   ├── main.js                        # Main site functions, forms, cart, navigation actions, translation callback
│   ├── tour-navigation.js             # Tour / itinerary helper
│   ├── relax-button.js                # Relax breathing button interaction and drag logic
│   ├── relax-integration.js           # Relax button positioning / integration
│   ├── back-to-top.js                 # Back-to-top button behavior
│   └── page-reveal.js                 # Initial page reveal / preload behavior
├── components/
│   ├── loading-screen.html            # Loading overlay markup reference
│   ├── relax-button.html              # Relax button markup reference
│   └── floating-actions.html          # Floating action buttons markup reference
└── assets/
    └── images/
        ├── image-01.webp ... image-10.webp  # All 10 embedded images extracted from uploaded HTML
        └── health-mix-lehya-placeholder.svg # Placeholder: original product photo was not supplied
```

## Important compatibility note

- `index.html` loads `css/main.css`, which contains every original CSS block in its original order. This preserves the existing appearance and avoids CSS cascade regressions.
- The named feature CSS files are separated working copies for focused future editing. They are not additionally loaded by default because their rules are already present in `main.css`; loading them too would duplicate CSS and could change the cascade.
- JavaScript files are loaded as classic scripts in the original dependency order. Do not add `type="module"` unless the inline `onclick` functions are migrated too.
- `loading.js` runs early, does not wait for `window.load`, and has a 2.2-second failsafe so third-party translation/network delays cannot keep the loading overlay stuck.
- Google Translate remains an external optional script. The website itself does not depend on it to dismiss the loader.

## Images

All 10 embedded images in the uploaded HTML were extracted to `assets/images/` and converted to WebP. The source HTML also referred to `dr-akhil-remesh.jpg` and `health-mix-lehya.jpg`, but those two files were not included in the upload. The doctor section now reuses the supplied couple portrait (`image-01.webp`). The Health Mix Lehya image uses an explicit placeholder; replace `assets/images/health-mix-lehya-placeholder.svg` with the real approved product photo and update the `src` in `index.html`.

### Image inventory

| File | Source image dimensions | Purpose / note |
|---|---:|---|
| `image-01.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-02.webp` | 1536 × 693 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-03.webp` | 768 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-04.webp` | 768 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-05.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-06.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-07.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-08.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-09.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |
| `image-10.webp` | 1536 × 1536 | Extracted from uploaded HTML; retain this filename unless updating its HTML reference. |

## Upload to GitHub

1. Create or open the website repository on GitHub.
2. Upload **all files and folders inside this project**, not just `index.html`.
3. Confirm the repository root contains `index.html`, `css/`, `js/`, `components/`, and `assets/`.
4. In GitHub, open **Settings → Pages**.
5. Select **Deploy from a branch**, choose `main` and `/ (root)`, then Save.
6. Open the published site and test desktop and mobile layouts, loading screen, all floating buttons, cart, consultation form, language selector, and image loading.

## Editing guide

- Website wording / section order: `index.html`
- Overall appearance: `css/main.css`
- Loading screen behavior: `js/loading.js` and `css/loading.css`
- Relax breathing button: `components/relax-button.html`, `js/relax-button.js`, `js/relax-integration.js`, `css/relax-button.css`
- Floating buttons: `components/floating-actions.html`, `css/floating-buttons.css`; button actions are defined in `js/main.js`
- Other button functions and cart: `js/main.js`
- Back to top: `js/back-to-top.js`
- Images: `assets/images/`

The original HTML was split and static source checks were performed. Live GitHub Pages deployment and real-device interaction tests must still be performed after upload.
