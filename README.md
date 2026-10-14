# Prime Physiotherapy & Sports Injury Clinic: website redesign

A fast, accessible, mobile-first redesign built as plain HTML, CSS and a little JavaScript.
No build step, no dependencies, so it hosts for free anywhere that serves static files.

```
index.html              the whole site (single page, anchor navigation)
assets/css/style.css    all styles (design tokens at the top, in :root)
assets/js/main.js       mobile menu, accordions, header shadow
favicon.svg
vercel.json             optional Vercel settings
.nojekyll               tells GitHub Pages to serve files as-is
```

## Deploy on GitHub Pages (free)

1. Create a new repository on GitHub and upload everything in this folder (keep `index.html` at the repo root).
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then Save.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

All asset paths are relative, so it works under that sub-path without changes.

## Deploy on Vercel (free Hobby plan)

**From GitHub:** push the folder to a repo, then in Vercel choose **Add New > Project**, import the repo, leave Framework Preset as **Other**, leave Build Command and Output Directory empty, and click Deploy.

**From the command line:** run `npx vercel` inside this folder and accept the defaults.

## Before it goes live on the clinic's domain

- **Remove the draft safeguard.** `index.html` contains `<meta name="robots" content="noindex, nofollow">` so a preview never competes with the real site in search. Delete that line at launch.
- **Check the open questions** in "Content to confirm with the clinic" below.
- **Add real photos.** The hero and "why us" panels use illustrations. To use photos instead, replace the `<svg>` inside `.hero-art` / `.why-art` with `<img src="assets/img/your-photo.jpg" alt="..." width="..." height="..." style="width:100%;height:100%;object-fit:cover">`.
- **Add the APA and NDIS badges.** The old site shows these logos but the text doesn't say what the clinic's status is, so they were left out. Add the official logos with the clinic's approved wording.
- **Update the JSON-LD** block in the `<head>` (it points at the clinic's real URL) and add opening hours once confirmed.
- **Booking** uses the clinic's Cliniko page (`prime.cliniko.com/bookings`) in an iframe, as the old site did.

## Content to confirm with the clinic

1. **First consultation length.** The old Appointments page says 30-45 minutes; the FAQ says 45-60. The redesign uses 30 to 45 minutes.
2. **Number of clinics.** The old home page says "8 different locations" and links a Kentmore clinic, but the Contact page lists five. The redesign shows the five listed with addresses.
3. **Camira postcode.** The old Contact page shows "QLD430D", an obvious typo. The redesign uses 4300.
4. **Opening hours** are not published anywhere on the old site, so none are shown.
5. **Old SEO leftovers.** The old pages' meta keywords mention London, Wimbledon and osteopathy, which look like template leftovers. They were not carried over.
