# RM Photography — Website

A scroll-driven Next.js site for RM Photography (Omaha photographer), built
in a warm/golden editorial style matching her actual portfolio.

## Before you run this

1. Run `download_rm_photos.py` (provided separately) to pull her real
   portfolio photos into `rm_photography_images/`.
2. Copy that folder's contents into `public/images/` here, keeping the
   same subfolder structure (`home/`, `about/`, `seniors/`, `families/`,
   `contact/`).
3. Open `app/components/ScrollHero.tsx` and confirm the `FRAMES` array
   filenames match what you actually have in `public/images/home/`.
   Reorder them however you'd like the scroll sequence to play.

## Run it

```bash
npm install
npm run dev
```

Then open http://localhost:3000

## Structure

- `app/components/ScrollHero.tsx` — full-screen scroll-scrubbed photo
  sequence (canvas + JPEGs, no video element, no scroll listeners — uses
  a requestAnimationFrame loop tied to scroll position)
- `app/components/ServicesSection.tsx` — Families / Seniors / Engagements
  / Weddings, replacing the generic "features" grid
- `app/components/InvestmentSection.tsx` — real pricing pulled from her
  current site
- `app/components/ClosingCTA.tsx` — contact CTA using her actual email

## Design tokens

| Token | Value |
|---|---|
| Background | `#FAF6F0` (warm cream) |
| Dark section bg | `#1A1410` |
| Accent (gold) | `#D8A857` |
| Text primary | `#2D2A26` |
| Text body | `#5C564C` |
| Display font | Playfair Display |
| Body font | Inter |

## Next steps you may want

- Swap in real wedding/engagement photos for the Services section cards
- Add a proper photo gallery/masonry page per service category
- Hook up the contact form to an email service (e.g. Formspree, Resend)
- Replace `mailto:` CTA with an embedded form once you pick one
