# Prabhupada Notes: website

The homepage and privacy policy for **Prabhupada Notes**, a free Chrome extension
for writing personal notes on the verses you read at
[vedabase.io](https://vedabase.io).

- Homepage: https://dev-notes-1896.github.io/prabhupada-notes/
- Privacy policy: https://dev-notes-1896.github.io/prabhupada-notes/privacy.html
- Questions and feedback: the homepage's [Help and feedback](https://dev-notes-1896.github.io/prabhupada-notes/#support) section (also the store's Support URL), or [issues](https://github.com/dev-notes-1896/prabhupada-notes/issues)
  or prabhupadanotes@gmail.com

The privacy policy URL is the one given to the Chrome Web Store and to Google's
sign-in setup, so it must stay at this address.

This repository holds only the website. The extension's source code is kept in a
separate repository.

## Files

```
index.html     Homepage: what the extension does, how it works, supported books, privacy summary
privacy.html   Privacy policy
style.css      Shared styles (vedabase palette, light and dark)
icon-128.png   Extension icon (page header, homepage)
icon-32.png    Favicon
.nojekyll      Serve files as-is (no Jekyll processing)
```

## Preview locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000/
```

Check both pages at desktop and phone widths, and in dark mode.

## Publish

GitHub Pages serves the `main` branch root. Pushing to `main` republishes the
site in about a minute; no build step.

## Rules for editing

- **No scripts, cookies, analytics, or third-party resources** (fonts, images, CDNs).
  The pages load only their own files. The privacy policy says so.
- **The privacy policy must match what the extension actually does.** If the
  extension's data handling, permissions, or network connections change, update
  `privacy.html` first and change its effective date (the "Changes" section
  promises this).
- **Keep both Limited Use statements** in the policy, worded exactly as they are:
  the Chrome Web Store one and the Google API Services one. Both programs require them.
- **Keep the non-affiliation statement**: the project is not affiliated with the
  Bhaktivedanta Book Trust or the Bhaktivedanta Archives.
- **Nothing personal.** Use only the project identity: "Prabhupada Notes",
  `prabhupadanotes@gmail.com`, and the `dev-notes-1896` account. Commit with the
  project's noreply identity:
  ```bash
  git config user.name "Prabhupada Notes"
  git config user.email "353989315+dev-notes-1896@users.noreply.github.com"
  ```

## Pending

- When the Chrome Web Store listing is live, replace the homepage's
  "Add to Chrome" placeholder (`<span class="cta" aria-disabled="true">`) with a
  link to the listing, and remove the "Coming soon" note.
- If the Google sign-in screen gets a logo, Google requires verifying this site's
  domain in Google Search Console. That's done by adding the verification
  `<meta>` tag it provides to `index.html`.
