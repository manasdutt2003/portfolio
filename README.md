# Manas Dutt — Portfolio Website

A single-page portfolio built in **plain HTML + CSS** (no JavaScript, no build step),
styled in the Perficient brand palette sampled directly from the capstone deck.

| Colour | Hex | Use |
|---|---|---|
| Perficient Teal | `#075056` | Page background, nav |
| Accent Shape | `#25656B` | Chevron motif, gradients |
| Aqua | `#5FD6C8` | Headlines, links, metrics |
| Abyss | `#02262A` | Section depth, button text |

## Files

```
Portfolio Website/
├── index.html      # the whole site: nav, hero, about, 5 capstones, 15 projects, skills, credentials, contact
├── style.css       # design system + layout + responsive + print styles
├── netlify.toml    # publish config and security headers
├── assets/         # profile-photo.jpg and Manas_Dutt_Resume.pdf go here
└── README.md
```

## Sections

1. **Hero** — name, role, stat strip (5 capstones · 1,100+ files · 900+ tests · $6.07M reconciled)
2. **About** — role at Perficient plus a facts table
3. **Capstones** — Weeks 1–5, each with real metrics, highlights and a repository deep link
4. **Projects** — 15 cards linking to public GitHub repositories
5. **Skills** — 8 capability groups
6. **Credentials** — experience and education
7. **Contact** — email, LinkedIn, GitHub

## Capstone links

The five weekly capstones live in the **private** `Perficient-Corporate/GGTP_CHN_DP_SEP_26`
repository, so those links open only for people signed in with Perficient org access.
Cards are marked *Internal repository* to set that expectation.

## Local preview

No server needed — open `index.html` in a browser. To serve it anyway:

```bash
python -m http.server 8000
```

## Deploying

Netlify, publishing this folder as-is (`netlify.toml` sets `publish = "."`).

```bash
npx netlify-cli deploy --prod --dir .
```

## Presenting

- Designed for projector contrast: large condensed display type, high-contrast aqua on deep teal.
- `Ctrl` + `-` / `+` scales cleanly; the layout reflows down to phone width.
- `Ctrl` + `P` produces a clean light-background PDF (print styles included).
- Respects `prefers-reduced-motion`.

## Swapping in the profile photo

Drop the image at `assets/profile-photo.jpg`, then in `index.html` replace:

```html
<div class="monogram">MD</div>
```

with:

```html
<img src="assets/profile-photo.jpg" alt="Manas Dutt">
```
