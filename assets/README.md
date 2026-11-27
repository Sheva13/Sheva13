# Farrel Sheva · Visual Asset System

This folder is the source of truth for the Farrel Sheva profile artwork. Placeholder vector files are now committed so the layout can be reviewed in place. Replace each file in this folder with your final artwork; keep the same file name, viewBox, and aspect ratio so the README does not shift.

The direction is **original marine modernism**: Fontaine-era restraint, Hydro fluidity, and abyssal depth. Do not use Furina's face, character renders, official game UI, copied sigils, or traced assets. The result should read as an independent developer identity first; the inspiration should be felt, not announced.

---

## Design Lenses

Every asset should balance three references without illustrating any of them literally:

- **Aristocratic restraint** — thin ornamental lines, symmetry, refined borders, generous negative space, and a single gold hairline where it earns its place.
- **Hydro motion** — flowing currents, orbital circles, translucent overlaps, and gradients that suggest depth rather than shine.
- **Abyssal marine life** — the manta ray as the primary silhouette; jellyfish, particles, and bioluminescent cyan as secondary marks.

If an asset reads as anime fan art, a generic tech banner, or decorative clip-art, it has gone too far in one direction. The target is a calm, premium developer identity with a marine memory.

## Hierarchy

- One focal point per asset: the manta in the banner, the crest in the logo, the diamond in the divider.
- Ornament supports the focal point; it never competes with it.
- Use no more than two accent colors in a single asset.
- Let negative space do as much work as the linework.

---

## 1. Palette

| Token | Hex | Role | Share |
| :--- | :--- | :--- | :--- |
| Midnight Navy | `#101E38` | Primary field / banner base | 35% |
| Deep Ocean | `#193D65` | Secondary field / depth | 25% |
| Hydro Blue | `#287FA5` | Currents / primary accent | 15% |
| Pearl White | `#F4F5F2` | Primary text / high contrast | 10% |
| Mist White | `#D9F3F3` | Hairlines / light details | 5% |
| Aqua Cyan | `#76C9D7` | Bioluminescent highlight | 6% |
| Silver | `#B7C8D5` | Secondary detail | 2% |
| Marine Steel | `#527C91` | Borders / muted detail | 1.5% |
| Champagne Gold | `#C5A76D` | Ornament only | 0.5% |

These proportions apply to the SVG artwork. GitHub controls the README's own text and background colors, so the README relies on typography and the vector assets for the visual identity.

**Rules**

- Gold never dominates. Keep it below 5% of any composition, ideally under 1%.
- Use Marine Steel for 1px borders and quiet details, not body text.
- Body text is Pearl White or Mist White. Avoid pure `#FFFFFF` and pure black.
- Check Hydro Blue on Deep Ocean before using it for text; it is safer as a line or fill accent.
- Pearl White on Midnight Navy has strong contrast. Aqua Cyan also works well on Midnight Navy. Gold is for small ornamental marks, not long text.

---

## 2. Typography

- **README:** GitHub's system font stack only. No custom CSS, webfonts, or JavaScript.
- **SVG display:** a high-contrast serif such as `Georgia, 'Times New Roman', serif` for a single wordmark, if one is needed. Labels may use `ui-monospace, 'SFMono-Regular', Consolas, monospace`.
- **Banner:** text-free by default. The README supplies the `Farrel Sheva` wordmark and tagline.
- **If text is used in SVG:** convert it to paths or use generic font families; never link an external font.
- **Letter spacing:** `0.16em–0.22em` for small uppercase labels; `0.01em–0.03em` for body text.
- **Weight:** 300–500. Avoid heavy black weights and faux italic.
- **Limit:** no more than two type sizes in the banner.

---

## 3. Asset Contract

| File | viewBox | Role | Status |
| :--- | :--- | :--- | :--- |
| `banner.svg` | `0 0 1600 500` | Hero above the wordmark | Placeholder — replace in place |
| `manta-ray.svg` | `0 0 512 512` | Avatar / monogram / social mark | Placeholder — replace in place |
| `hydro-divider.svg` | `0 0 1200 48` | Section break | Placeholder — replace in place |
| `wave-pattern.svg` | `0 0 1600 600` | README texture strip / personal site | Placeholder — replace in place |
| `ornaments.svg` | `0 0 1200 120` | Section mark divider | Placeholder — replace in place |
| `jellyfish.svg` | `0 0 256 384` | Secondary motif | Placeholder — replace in place |
| `footer.svg` | `0 0 1600 240` | Footer strip | Placeholder — replace in place |

**Common requirements**

- Include `role="img"`, `<title>`, and `<desc>` in every SVG.
- Use a `viewBox`; include `width` and `height` for fallback rendering.
- No external `<image>`, fonts, scripts, or stylesheets.
- No raster images, stock photography, or traced official artwork.
- Keep the geometry readable at 320px wide. Remove details that turn to noise at small sizes.
- Transparent assets must remain visible on both light and dark backgrounds; prefer Hydro Blue or Marine Steel for hairlines, with Aqua Cyan as an accent.
- Prefer gradients, opacity, and clean geometry over heavy blur filters.

---

## 4. Composition Notes

### Banner — `banner.svg`

- Canvas: `1600 × 500`. Horizon around 62% height.
- Manta: centered near `800, 250`; wingspan 600–680; abstract and geometric, not photoreal.
- Ring: a thin orbital ellipse around the manta, `rx` 340–380 and `ry` 190–220, centered at `800, 250`; keep it inside the canvas.
- Currents: three to five parallel cubic Bézier lines behind the manta; vary opacity between 0.08 and 0.35.
- Particles: eight to fourteen tiny pearl or cyan dots at varied opacity; they should read as depth, not glitter.
- Texture: fine dot grain or subtle noise only; no photographic water textures.
- Ornament: four restrained corner details at a 64px inset; one or two gold hairlines at most.
- Negative space: keep roughly 18% clear on each side so the composition survives a narrow mobile crop.
- Text: none. The README wordmark sits below the banner.

### Manta Ray — `manta-ray.svg`

- A dark navy rounded-square crest with a thin silver/pearl border and a pearl/cyan manta is the safest way to work on both dark and light backgrounds.
- Recognizable at 32px: simplify to five to seven primary shapes.
- Wing tips swept back; cephalic fins forward; tail as one tapered curve.
- Use negative space for the underside. Avoid literal eyes or a mouth; a small pearl node can suggest the head.
- No text. The mark must not resemble an existing copyrighted logo.

### Hydro Divider — `hydro-divider.svg`

- Transparent canvas, symmetric composition, 1px hairlines.
- Center diamond or small pearl node, flanked by two or three current lines.
- Works as a quiet section break at full width or at 320px.

### Wave Pattern — `wave-pattern.svg`

- Seamless or visually tileable; low contrast; transparent background.
- Three to five parallel currents with different opacities.
- No literal foam, spray, or photographic water texture.
- Intended as an optional texture strip or a personal-site background, not a busy README decoration.

### Ornaments — `ornaments.svg`

- Four mirrored corner pieces built with `<symbol>` and `<use>`.
- Original "hydro fleur" motif: a central diamond, two mirrored C-scrolls, three tapered leaves, and small dot terminals.
- Do not copy the Fontaine crest, the Hydro sigil, or any Genshin Impact insignia.
- Gold is limited to tiny terminals or a single hairline.

### Jellyfish — `jellyfish.svg` (optional)

- Line-art only; no face, no character styling.
- Bell as a thin arc; five to seven tentacles with varying lengths.
- Cyan bioluminescence via a soft radial gradient, not a heavy blur.
- Transparent background; works as a small secondary mark.

### Footer — `footer.svg`

- Canvas: `1600 × 240`. Mirrored currents and a smaller manta silhouette.
- One gold hairline, no text. The README supplies the closing line.

---

## 5. GitHub Integration

Placeholder artwork is already wired into `README.md`. Replace each file in place; keep the same file name, viewBox, and aspect ratio so the layout does not shift.

Current placements:

| Asset | Placement |
| :--- | :--- |
| `banner.svg` | Top hero, full width |
| `manta-ray.svg` | 72px monogram above the wordmark |
| `hydro-divider.svg` | Full-width divider after the header |
| `wave-pattern.svg` | Full-width 100px strip after About Me |
| `ornaments.svg` | Full-width divider before Connect |
| `jellyfish.svg` | 96px secondary mark above the footer |
| `footer.svg` | Full-width footer strip |

The final banner and footer should be text-free; the README supplies the name and closing line. The current placeholders carry a small label so they are easy to identify and replace.

### Profile settings (manual)

- **Avatar:** export `manta-ray.svg` to a 512×512 PNG. GitHub's avatar uploader expects PNG, JPG, or GIF, not SVG.
- **Social preview:** export `banner.svg` to a 1280×640 PNG or JPG, then upload it in repository settings.
- **Pinned repositories:** pin `chess_review`, `management-app`, `ai_citra`, and `UAS-URL-Checker`.
- **Bio:** add a short line such as “Informatics student building local-first web, mobile, and ML tools.” Only publish details you want public.
- **Contact:** add email, LinkedIn, or a personal site in GitHub settings when available, then add the same link to the README's Connect section.

### Keep it restrained

- No visitor counters, contribution snakes, trophy widgets, or badge walls.
- No external badge services that can fail or clutter the typography.
- No more than one focal point per asset.
- The profile must still read as a developer portfolio if the marine motifs are removed.

---

## 6. Accessibility

- Every SVG includes `role="img"`, a unique `<title>`, and a `<desc>` that explains the composition.
- README alt text matches the SVG's meaning; decorative assets use `alt=""`.
- Do not convey essential meaning through color alone; pair accents with shape or position.
- Keep text at least 12px at 1×, or convert it to paths.
- Avoid animation. If motion is used, keep it subtle and respect `prefers-reduced-motion`.
- Test the profile with images disabled; the text must still tell the whole story.

---

## 7. Validation Checklist

- [ ] `xmllint --noout assets/*.svg` passes.
- [ ] Each SVG opens in a browser at 320px, 768px, and 1440px.
- [ ] The composition works on GitHub dark and light themes.
- [ ] Text in SVG is at least 12px at 1×, or converted to paths.
- [ ] No external `href`, `<image>`, fonts, scripts, or stylesheets.
- [ ] Every SVG has `role="img"`, `<title>`, and `<desc>`.
- [ ] File names and relative paths match exactly; GitHub paths are case-sensitive.
- [ ] The README remains readable with images disabled.
- [ ] Gold remains a minor accent, never a dominant field.
- [ ] No Furina face, official render, game logo, Hydro sigil, or Fontaine crest appears anywhere.

---

## 8. Originality Guardrails

- No character illustrations, portraits, hair, hats, outfits, or official renders.
- No Genshin Impact logos, UI frames, elemental sigils, or Fontaine heraldry.
- No traced or recolored official artwork.
- No stock manta ray photographs; original vector geometry only.
- No gold-dominant palette, no ornamental overload, no anime fan-page framing.
- The identity should survive as a professional developer brand even without the marine motifs.
