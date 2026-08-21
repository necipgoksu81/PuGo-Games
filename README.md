# PuGo Games — pugogames.com

Static marketing and legal site for **PuGo Games**, served from GitHub Pages
on the custom domain in `CNAME`.

## Pages

| Path        | Purpose                                                        |
|-------------|----------------------------------------------------------------|
| `/`         | Studio homepage — hero, Zing Blast! showcase, about, contact |
| `/privacy/` | Privacy Policy (linked from the Google Play listing and in-game) |
| `/terms/`   | Terms of Service (linked from the in-game settings panel)        |

The Play Console listing and the game's Settings → More Settings panel both point
at `/privacy/` and `/terms/`, so those two URLs must not change.

## Files

```
index.html              homepage
privacy/index.html      privacy policy   (legal copy — edit text only)
terms/index.html        terms of service (legal copy — edit text only)
style.css               all styling for every page
site.js                 sticky nav, mobile menu, scroll reveal (progressive)
CNAME                   custom domain for GitHub Pages

pugo-wordmark.png       white PuGo Games wordmark  (dark backgrounds)
pugo-wordmark-ink.png   deep violet wordmark       (light backgrounds)
zing-blast-logo.png     Zing Blast! game logo
zing-blast-icon.png     app icon, 512×512
pugo-icon.png           PuGo Games favicon, 512×512 (white mark on violet)
shot-1..4.png           gameplay screenshots, caption bars cropped off
```

`pugo-logo.png`, `pugo-logos.png`, `slide-block-jam-icon.png`, `sbj-logo.png` and
`sbj-icon.png` are full-resolution or superseded originals. They are no longer
referenced by any page and can be removed if you want a leaner repo.

## Notes

- No build step, no dependencies. Push to the default branch and GitHub Pages
  serves it as-is.
- `site.js` is purely progressive: with JavaScript disabled every section is
  still fully visible and every link still works.
- Fonts (Baloo 2, Manrope) load from Google Fonts.
- The Google Play button points at
  `play.google.com/store/apps/details?id=com.pugogames.slideblockjam`. The game
  went live in production on 21 August 2026, so that link resolves.
- `app-ads.txt` must stay at the repository root. AdMob verifies app ownership by
  fetching `pugogames.com/app-ads.txt`, so moving or deleting it breaks
  verification and ad serving.

## Editing the legal pages

Both legal pages keep their content inside a single `<div class="legal-wrap">`.
Edit only the text inside that block; the surrounding header, hero and footer are
shared markup and should stay in sync with `index.html`.

The page title and "Last Updated" line are written once inside `.legal-wrap` and
repeated in the `.legal-hero` block at the top. `style.css` hides the copy inside
`.legal-wrap`, so if you change the date, change it in **both** places.

---

© 2026 PuGo Games
