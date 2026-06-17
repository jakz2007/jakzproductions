# Jakz Productions – Portfolio Website

A static HTML/CSS portfolio site to replace the Carrd version.  
Works with any web host (Netlify, Vercel, GitHub Pages, or your own server via FTP).

---

## File structure

```
jakz-productions/
├── index.html        ← main page
├── style.css         ← all styles
├── README.md         ← this file
└── assets/           ← put your images here
    ├── logo.png           ← the JP logo (top of hero)
    ├── logo-wordmark.png  ← "JAKZ PRODUCTIONS" text logo (footer)
    └── tgg-avatar.png     ← TGG gorilla avatar (testimonial)
```

---

## Quick setup checklist

### 1 — Add your logo files
Create an `assets/` folder next to `index.html` and drop in:
- `logo.png` – the circular JP logo used in the hero
- `logo-wordmark.png` – the "JAKZ PRODUCTIONS" stacked wordmark used in the footer
- `tgg-avatar.png` – the red gorilla avatar for the TGG testimonial

### 2 — Swap in real YouTube video IDs
In `index.html`, find each `src="https://www.youtube.com/embed/VIDEO_ID_X"` placeholder and replace the `VIDEO_ID_X` part with the actual YouTube video ID.

Example:  
`https://www.youtube.com/watch?v=dQw4w9WgXcQ`  →  ID is `dQw4w9WgXcQ`  
So use: `src="https://www.youtube.com/embed/dQw4w9WgXcQ"`

There are 5 iframes to update:
| Placeholder    | Which video                          |
|----------------|--------------------------------------|
| `VIDEO_ID`     | Your showreel (hero section)         |
| `VIDEO_ID_1`   | AnyMelody – 9.3M subs video          |
| `VIDEO_ID_2`   | TGG – Rags 2 Riches / 2.8M views     |
| `VIDEO_ID_3`   | TGG – GTA map video / 2.1M views     |
| `VIDEO_ID_4`   | YDE – 250K subs video                |

### 3 — Update the Twitter DM link
Search for `https://twitter.com/JakzProductions` in `index.html` (appears twice) and replace with your actual Twitter/X URL.

### 4 — Add a favicon (optional)
Drop a `favicon.ico` or `favicon.png` into `assets/` and uncomment the `<link rel="icon">` line in the `<head>` of `index.html`.

---

## Deployment options

### Netlify (recommended – free)
1. Go to https://netlify.com → New site from folder
2. Drag and drop the entire `jakz-productions/` folder
3. Set your custom domain in Site Settings → Domain Management

### GitHub Pages (free)
1. Push this folder to a GitHub repo
2. Settings → Pages → Source: main branch / root
3. Add custom domain in the Pages settings

### Your own hosting via FTP
Upload all files (preserving the folder structure) to your web root (`public_html/` or `www/`).

---

## Adding more portfolio entries

Copy one of the `<div class="port-entry ...">` blocks in `index.html` and update the video ID, name, and stat. Entries automatically alternate left/right based on the `port-entry--left` / `port-entry--right` class.

## Adding more testimonials

Copy the `<div class="testimonial-card">` block and update the name, quote, and avatar image.
