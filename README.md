# zotebook-site

Marketing site for [Zotebook](https://github.com/Klectr/zotebook), the plain editor for folders of Markdown files.

Served at [zotebook.klectr.dev](https://zotebook.klectr.dev) from the Klectr VPS (`/var/www/zotebook`, nginx, TLS at Cloudflare).

## Editing

Static files, no build step: `index.html` and `img/`. Edit, commit, and copy them to the VPS:

```
scp -r index.html img root@<vps>:/var/www/zotebook/
```

Design: the DeepSeek Harness system (near-black hero with a coloured glow, white pill CTAs, Montserrat/DM Sans/Fragment Mono, 1080px container), the same treatment as zlab.klectr.dev and zlorb.klectr.dev, with Zotebook's violet (`#7A4FBA`) as the accent.

- The screenshots in `img/` are real app renders, taken headlessly from the release build on a sample notes folder and converted to WebP with `cwebp -q 82 -resize 1920 0`.
- `img/og-image.png` (1200×630) is composed as SVG and rendered with `rsvg-convert`.
- The brand marks come from `assets/brand/` in the Zotebook repository.
