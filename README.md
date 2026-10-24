# App Legal Website

A lightweight, responsive static website for an educational Android application. This project is being added to the existing `app-legal-website` repository; no new repository was created.

## Files

- `index.html` — homepage
- `privacy-policy/index.html` — privacy policy draft
- `terms-of-service/index.html` — terms of service draft
- `assets/styles.css` — responsive styles, dark-mode support, and reduced-motion/accessibility rules

No backend, database, authentication, analytics, Supabase, APK distribution, or build step is included. The site uses only HTML, CSS, and a tiny inline script to update the copyright year.

## Preview locally

From the project root, run a static file server, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`. The directory-based routes work with static hosts that serve `index.html` from folders.

## Static deployment

Deploy the existing repository's root directory to a static hosting provider such as Cloudflare Pages. No build command is required; the output/root directory is `/` (the repository root). Do not configure a custom domain or publish until the launch checklist below is complete.

For GitHub Pages, enable Pages for the intended branch and root directory in repository settings. A custom domain and HTTPS should be configured only if you own/control that domain. Confirm the provider serves folder routes directly and enforces HTTPS.

## Required launch checklist — do not skip

The legal pages are deliberately marked as drafts and set to `noindex, nofollow`. Do **not** submit their URLs to Google Cloud Console or treat the site as production-ready until:

1. Replace every `[APPLICATION NAME]` token with the confirmed product name.
2. Confirm the app's real features and intended audience.
3. Review the Android source/dependencies and runtime behavior for data collection, account creation, Google Sign-In, local/remote storage, SDKs, analytics, crash reporting, file/device permissions, sharing, and deletion.
4. Complete and approve the privacy policy based on those verified facts.
5. Confirm content ownership/licensing, actual app functionality, responsible operator, contact method, and applicable jurisdiction; finalize the terms accordingly.
6. Set accurate effective dates, remove the draft warning boxes and `noindex` metadata from the legal pages only after approval.
7. Test the homepage, both legal routes, direct URL refreshes, navigation, mobile layout, and HTTPS on the deployed domain.

No developer contact details, company identity, or domain have been invented.

## Intended public URLs after deployment

Replace `YOUR-DOMAIN` with your actual HTTPS domain:

- Homepage: `https://YOUR-DOMAIN/`
- Privacy Policy: `https://YOUR-DOMAIN/privacy-policy/`
- Terms of Service: `https://YOUR-DOMAIN/terms-of-service/`

The route without a trailing slash may redirect depending on the host. Configure and test the final canonical URLs before entering them in Google Cloud Console.
