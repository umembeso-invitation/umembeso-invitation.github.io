# Wedding Invitation Site

A single static site — no build step, no framework. Just open `index.html` in
VS Code and edit directly.

## Files

- `index.html` — all page content
- `style.css` — all styling (colors, fonts, layout)
- `script.js` — mobile nav toggle only

## What to edit before launch

Search the project for `PLACEHOLDER` and `[` to find every spot that needs
your real details:

1. **Partner's name** — in the `<title>`, hero, and footer
2. **Wedding date, city** — hero section
3. **Venue date/time, name, address, dress code** — `#details` section
4. **Google Maps embed** — replace `PLACEHOLDER_MAP_EMBED` in the iframe `src`,
   and `PLACEHOLDER_VENUE_NAME` in the fallback link, both inside `#details`.
   In Google Maps: search your venue → **Share → Embed a map** → copy the
   `src="..."` value out of the provided `<iframe>` code.
5. **RSVP deadline** — `#rsvp` section
6. **Google Form embed link** — replace `PLACEHOLDER_FORM_ID` in **two**
   places inside the `#rsvp` section (the iframe `src` and the fallback link)
   with your own form's ID. In Google Forms: **Send → the `<>` embed icon →
   copy the `src="..."` value** out of the provided `<iframe>` snippet.
7. **YuppieChef registry link** — replace the `PLACEHOLDER` URL in the
   `#registry` section with your actual registry link
8. **Contact email** — footer

The monogram currently reads "T&P" — update the `<text>` content inside
the two `<svg class="monogram__svg">` blocks in `index.html` to match your
initials.

## Running it locally

Just open `index.html` in a browser — no server or build tools needed.
For live-reload while editing, the VS Code "Live Server" extension works well.

## Deploying to GitHub Pages (free)

1. Create a new GitHub repository and push these three files (`index.html`,
   `style.css`, `script.js`) to the root of the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
4. GitHub gives you a URL like `https://yourusername.github.io/repo-name/`
   within a minute or two.
5. **Custom domain (optional):** if you bought a domain (e.g. from
   Domains.co.za, Afrihost, or Namecheap), add it in the same Pages settings
   screen under "Custom domain", then create the DNS records your registrar's
   docs specify (usually a `CNAME` record pointing to
   `yourusername.github.io`, or four `A` records for an apex domain —
   GitHub's Pages docs list the current IPs).

## RSVP responses

Every RSVP submitted through the embedded Google Form lands automatically in
a Google Sheet — open the form in Google Forms and check the **Responses**
tab, or click the sheet icon there to create a linked spreadsheet.

## Taking the site down after the wedding

GitHub Pages is free indefinitely, so there's no rush — but if you registered
a domain just for this, you can simply let it lapse/not renew after your
event rather than cancelling anything mid-term.
