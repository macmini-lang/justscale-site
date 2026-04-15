# Pure Auto Care — Website

Single-file static site. Deploy like JustScale: drop into a GitHub repo, add `CNAME`, point domain at GitHub Pages.

## Before ship — fill these placeholders

Search `index.html` for `{{...}}` and replace:

- `{{PHONE_RAW}}` — phone for `tel:` links, digits only (e.g. `14065551234`)
- `{{PHONE_DISPLAY}}` — phone displayed to users (e.g. `(406) 555-1234`)
- `{{EMAIL}}` — contact email
- `{{SERVICE_AREA}}` — e.g. `Bozeman, MT & surrounding area`
- `{{HOURS}}` — e.g. `Mon–Sat, 8am–6pm`
- `{{MOBILE_OR_SHOP_LINE}}` — short line in step 2. Pick one:
  - Mobile only: `We come to you — home, work, wherever the car lives.`
  - Shop only: `Drop the car at our shop and we'll text you when it's ready.`
  - Both: `Mobile or in-shop — your call. We bring everything either way.`
- `{{MOBILE_OR_SHOP_ANSWER}}` — longer FAQ answer on same topic
- `{{REVIEW_1_BODY/NAME/META}}` × 3 — pull real reviews from Google/IG DMs
- `{{FORM_ENDPOINT}}` — form handler. Options:
  - Formspree: `https://formspree.io/f/YOUR_ID` (free tier works)
  - Basin, Getform, Web3Forms — any form-to-email service
  - GHL webhook if Pure has a CRM
  - Leave blank and the JS shows a success message (but form data is lost — do not ship like this)

## Verify before ship

- Confirm IG handle is `@autocarebypure` (current placeholder in gallery + footer)
- Confirm service prices match current offering
- Ask Pure if they do mobile, shop, or both — rewrites the process + FAQ copy
- Swap gallery placeholders for 8 real before/after photos (1:1 ratio works best)
- Add a real logo — current header is a text wordmark `Pure. Auto Care` using Anton font. Drop a `logo.svg` in this folder and replace the `.nav__logo` div if you want an image mark.

## Design

- Fonts: Anton (display) + Inter (body) — loaded from Google Fonts
- Palette: `#D40000` red, `#0A0A0A` black, `#F6F4F1` warm off-white
- Fully responsive, single HTML file, ~1 req to render (plus fonts)
- No framework, no build step

## Deploy

```bash
cd /Users/zacregan/Jarvis/agency/website/pure-auto-care
# create GitHub repo, push
# add CNAME file with chosen domain (e.g. pureautocare.com)
# point DNS A records at GitHub Pages, enable Pages in repo settings
```

Or host on Netlify / Vercel / Cloudflare Pages — drag-and-drop the folder.
