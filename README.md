# Homeground

Mobile-first, buildless HTML/CSS/JavaScript prototype for a speculative Singapore cultural experience centre in 2050. This independent final-year design concept is not a government service. No backend, runtime API or payment integration.

## Run

Open `index.html` directly, or use `python3 -m http.server 8765` in this directory and visit http://localhost:8765. A local server is recommended for consistent browser storage. All artwork, fonts and QR generation code are bundled locally.

## Features

- Five accessible bottom navigation destinations with hash-based deep links.
- Four-step simulated booking, illustrative capacity of 60 per session, adult/child counts, validated visitor details, QR pass and offline HTML pass download.
- Six individual experience pages and original single-floor spatial plan.
- Editable passport details and four optional manually recorded stamps.
- 28 searchable Singlish phrases, category filters, device-local favourites, random discovery and free-play sentence builder.
- Device speech synthesis where supported; pronunciation depends on installed voices.
- Browser-local persistence for bookings, passport details, stamps and favourites.

All booking dates deliberately use the speculative 2050 season. Initial availability is deterministic illustrative data; bookings created on this device reduce its remaining capacity. Nothing is reserved globally. QR codes encode only a demo booking reference, not personal information. Downloaded passes are not valid for admission. Stamps form one visitor keepsake and can be manually undone; booking another visit does not automatically erase them.

## GitHub Pages

1. Create or grant access to `aliasgeradamally/Homeground`.
2. Push this directory's contents to the `main` branch.
3. In repository Settings → Pages, select **GitHub Actions** as the source.
4. The included `pages.yml` workflow deploys the app on pushes to `main`, or by manual dispatch.

Expected URL after successful deployment: `https://aliasgeradamally.github.io/Homeground/` (not published at delivery).

## Verification

JavaScript syntax and automated logic checks passed. Asset existence, image decoding and route rendering were checked. Browser visual QA and end-to-end interaction testing were blocked by browser permission denial in the development session. GitHub repository creation/push/deployment were also blocked; this package must not be described as published.

## Assets and attribution

Original orchid–HDB logo and brand illustrations are extracted as rectangular crops from user-supplied brand artwork without redrawing or recolouring. Passport logo is extracted from the supplied physical passport reference. Interior/exterior concepts and spatial layout are user-supplied, resized/compressed for delivery without redesign. The original illustrations contain their own source colours/textures; application UI uses the four specified brand colours.

Display font: Fraunces by Undercase Type, SIL Open Font License; locally bundled. Supporting type uses system Arial/Helvetica. QR generator: qrcode-generator 1.4.4 by Kazuhiko Arase, MIT license, preserved in the source header. See `assets/Fraunces-OFL.txt`.

## Visual refinement — November 2026

Supporting text now requests locally available Aptos, with Segoe UI, Calibri and system sans-serif fallbacks. Proprietary font files are not bundled. Serif display headings are unchanged. Primary and secondary actions share a 52px height and 216px desktop width; peer controls align evenly and actions fill their mobile container. Functional filters remain; decorative pills and repeated footer explanations were removed. Repeated prototype notices and explanatory footnotes have been removed from the interface.

The illustration strip uses a high-resolution transparent edit, presented through a tightly cropped SVG viewport without raster resampling. The header now uses assets/logo-transparent.png with real alpha transparency instead of blending the paper background. The original source asset is retained. Interior photos remain at their supplied resolution with consistent responsive crops.

Image edit used the built-in image generation tool. Prompt: Remove the cream paper background and clipped heading from the original illustration strip, preserve HDB buildings, shrubs, MRT train, umbrella and communal table; retain intentional cream interiors; output high-resolution alpha transparency. Second pass: clean stray edge fragments and preserve the composition. Final asset: assets/illustrations-clean.svg, embedding the edited PNG.

Browser inspection remains blocked by a saved local-origin permission. Route rendering, asset references and JavaScript syntax were checked directly.

Header logo background removal: built-in image editing, preserving the orchid–HDB emblem and homeground. lettering while removing the cream paper background. Transparent corners and alpha pixels were checked directly.

Passport logo uses assets/passport-logo-transparent.svg, embedding the original artwork with an alpha colour mask, preserving its original geometry. Generated passport alternatives were rejected for visible edge artifacts.

## Copy cleanup

Removed repeated disclaimers and non-essential helper notes throughout booking, passport and Singlish. The information panel now describes Homeground and its experiences. Removed clear-data buttons and their event handlers without deleting any existing visitor data. Booking, availability and passport functionality remain browser-local simulations as documented above.

## Mobile layout and home-screen icons

The mobile navigation is inset 14px from the sides and 12px above the bottom safe area. Mobile headings, card padding, photos and passport stamps are more compact; main controls are 48px tall and input text stays at 16px.

manifest.webmanifest provides a relative start URL and scope for GitHub Pages. The app icon uses the existing orchid–HDB emblem without the wordmark, on warm cream. PNG sizes include 192px, 512px, a separately padded 512px maskable version, a 180px Apple touch icon and a 32px favicon. Editable SVG sources are included. No runtime icon-generation dependency or service worker was added.

Upload manifest.webmanifest and assets/icons alongside the updated HTML, CSS and JavaScript. Existing home-screen shortcuts may retain cached artwork; re-add the shortcut if necessary after publication.
