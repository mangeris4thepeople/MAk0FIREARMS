# MAk0Firearms — Website

Single-file site for MAk0Firearms, 1180 E. 3rd St., Loveland, CO 80537.
Green-phosphor DOS theme. No build step, no dependencies — pure HTML/CSS/JS.

## Files

| File          | Purpose                                              |
|---------------|------------------------------------------------------|
| `index.html`  | The entire site (styles, pages, inventory data, JS)  |
| `404.html`    | DOS-styled "file not found" page                     |
| `favicon.svg` | Browser-tab icon (amber crosshair)                   |
| `robots.txt`  | Search-engine permissions                            |
| `sitemap.xml` | Search-engine index hint                             |
| `.nojekyll`   | Tells GitHub Pages to serve files as-is              |

## Publish on GitHub Pages (free, ~5 minutes)

1. Sign in at **github.com** → click **+** (top right) → **New repository**
   - Name: `mak0firearms` (or anything)
   - Visibility: **Public** (required for free Pages)
   - Click **Create repository**
2. On the new repo page, click **uploading an existing file**
   - Drag in ALL files from this folder (including `.nojekyll`)
   - Click **Commit changes**
3. Go to **Settings → Pages** (left sidebar)
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)** → **Save**
4. Wait 1–2 minutes. Your site is live at:
   `https://www.mak0firearms.com/`

## After it's live (10-minute checklist)

- [ ] **Forms**: create a free account at formspree.io, make two forms
      (contact + special order), then search `index.html` for
      `YOUR_FORM_ID` (2 places) and paste in your real form IDs.
- [ ] **URLs**: search `index.html` for `mak0firearms.example` and replace
      with your live URL. Do the same in `robots.txt` and `sitemap.xml`.
- [ ] **Phone**: search for `970) 430-5884` / `+19704305884` and replace
      with your real number (appears in header schema, contact page,
      call button, footer).
- [ ] **Email**: replace `@mak0firearms.example` addresses with real ones.
- [ ] **Hours**: confirm the hours in the JSON-LD block (top of
      `index.html`) and on the contact page match your actual hours.

## Custom domain (optional)

Buy a domain (e.g. mak0firearms.com), then in **Settings → Pages →
Custom domain** enter it and follow GitHub's DNS instructions
(four A records + a CNAME at your registrar). GitHub provisions free
HTTPS automatically.

## Editing the site

Everything is commented by section inside `index.html`:

- **Products** — edit the `PRODUCTS` array in the `<script>` block.
  Set `stock:false` to show "CALL FOR ETA", `type:"firearm"` to force
  in-store pickup / FFL routing.
- **Featured grid** — currently replaced by the SOLD OUT cell; the
  restore instructions are commented next to it in the script.
- **Theme** — colors/fonts live in `:root`; the entire CRT effect is the
  block labeled `15. DOS / CRT THEME OVERRIDES` and can be tuned or
  deleted independently.

## Compliance notes

The site never sells or ships a firearm online. Firearms are "reserved"
and completed in person (Form 4473 + CBI background check + Colorado
waiting period). Keep that flow intact in any future edits.
