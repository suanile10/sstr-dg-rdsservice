# Master Prompt — SS Trädgårdsservice AB Landing Page

Copy everything inside the block below into Claude or ChatGPT.

---

## WEBSITE BUILD PROMPT

```
You are a senior web designer/developer. Build a complete, production-ready landing page as a SINGLE self-contained HTML file (all CSS and JS inline, no build tools, no external frameworks except Google Fonts). The page must be in SWEDISH.

## Client
SS Trädgårdsservice AB — an established garden maintenance company (trädgårdsskötsel) in Solna, Stockholm. Founded 2005, ~17 employees, serving property owners, BRFs (housing cooperatives), businesses and private homes in Solna and greater Stockholm.

Contact details to use:
- Adress: Virebergsvägen 15, 169 30 Solna
- Telefon: 073-332 06 53
- Org.nr: 556690-4784
- Badge: "F-skatt & momsregistrerad" and "Grundat 2005 — 20+ år i branschen"

## Design direction
- Style: modern, clean, premium but approachable. Think Scandinavian minimalism meets nature.
- Colors: deep forest green (#1E4D2B) as primary, warm off-white (#FAF8F3) background, soft sage (#A8BFA0) accents, one warm highlight color (#D9A441, muted gold) for CTAs.
- Typography: a friendly serif or rounded sans for headings (e.g. "Fraunces" or "Sora" from Google Fonts), clean sans for body (e.g. "Inter").
- Generous whitespace, large rounded corners (16–24px), soft shadows, subtle scroll-reveal animations (IntersectionObserver, CSS transitions only).
- Fully responsive (mobile-first), semantic HTML5, accessible (WCAG AA contrast, alt texts, aria labels).
- Add subtle organic decorative elements: leaf SVG shapes, curved section dividers.

## Page sections (in order)

1. **Sticky header** — logo text "SS Trädgårdsservice", nav links (Tjänster, Om oss, Referenser, Kontakt), phone number as click-to-call button.

2. **Hero** — full-viewport with background image placeholder (id="hero-img"). Headline: "Vi tar hand om din trädgård — året runt". Subline about 20 års erfarenhet i Solna & Stockholm. Two CTAs: "Begär offert" (primary) and "Ring oss" (secondary). Trust row beneath: "20+ år i branschen · 17 anställda · F-skattsedel".

3. **Tjänster (Services)** — 6 cards with icons (inline SVG):
   - Trädgårdsskötsel & underhåll (gräsklippning, häckklippning, rabatter)
   - Beskärning & trädvård
   - Plantering & anläggning
   - Höst- & vårstädning
   - Snöröjning & halkbekämpning (vintertjänst)
   - Skötselavtal för BRF & fastighetsbolag

4. **Varför välja oss** — 4 value props with numbers: 20+ år erfarenhet, 17 utbildade medarbetare, fasta priser & avtal, fullt försäkrade.

5. **Så funkar det** — 3 steps: Kontakta oss → Kostnadsfri besiktning & offert → Vi sätter igång.

6. **Referenser** — 3 realistic placeholder testimonials from a BRF chairman, a villa owner in Solna, and a property manager. Mark clearly in code comments as PLACEHOLDER — replace with real quotes.

7. **Om oss** — short company story (familjeföretag, grundat 2005, lokalt förankrat i Solna) with image placeholder (id="about-img").

8. **CTA-band** — full-width green band: "Redo att ge din trädgård den omsorg den förtjänar?" + offert button.

9. **Kontakt** — contact form (Namn, E-post, Telefon, Meddelande, dropdown for tjänst) with client-side validation, plus contact info card and embedded Google Maps iframe for Virebergsvägen 15, Solna.

10. **Footer** — contact details, org.nr, öppettider, nav links, copyright.

## Technical requirements
- All images as <img> with descriptive ids and alt text so they can be swapped easily; use https://placehold.co placeholders sized correctly.
- Smooth scroll for anchor links, mobile hamburger menu, form submits to mailto: as fallback (comment where to plug in a real endpoint).
- SEO: title "Trädgårdsskötsel i Solna & Stockholm | SS Trädgårdsservice AB", meta description in Swedish, Open Graph tags, JSON-LD LocalBusiness schema with the real address and phone.
- Page weight small, no jQuery, no external JS libraries.

Output the complete HTML file, nothing else.
```

---

## IMAGE GENERATION PROMPTS

Use with Midjourney, DALL-E, Flux, or Ideogram. Generate at 16:9 for hero, 4:3 or 1:1 for others. Keep a consistent look: natural light, green/earthy palette, Scandinavian setting.

**1. Hero image (`hero-img`, ~1920×1080)**
```
Professional gardener in dark green work clothes trimming a neat hedge in a lush Swedish residential garden, golden morning light, modern Scandinavian villa softly blurred in background, vibrant greens, shallow depth of field, photorealistic, editorial photography style, 16:9
```

**2. About section (`about-img`, ~800×600)**
```
Small friendly team of Swedish landscapers in matching green uniforms standing by a work van with gardening tools, suburban Stockholm street with birch trees, natural daylight, candid documentary photography style, warm and trustworthy mood, 4:3
```

**3. Service card — trädgårdsskötsel**
```
Close-up of gloved hands planting flowers in a well-kept perennial border, rich soil, soft bokeh green background, natural light, photorealistic macro photography, 1:1
```

**4. Service card — beskärning/trädvård**
```
Arborist pruning an apple tree with professional secateurs, Swedish garden in spring, blue sky, crisp detail, photorealistic, 1:1
```

**5. Service card — vintertjänst**
```
Snow removal on a residential walkway in a Swedish suburb, person in green winter workwear with snow shovel, fresh snow on hedges, soft overcast winter light, photorealistic, 1:1
```

**6. CTA-band background (~1920×600, darkened)**
```
Wide shot of a perfectly maintained lawn and flowerbeds outside a Swedish apartment building (BRF), evening golden hour, lush and orderly, slightly dark and moody so white text overlays remain readable, 16:9
```

**Tips:** add `--ar 16:9` / `--ar 1:1` in Midjourney; ask for "no visible faces" if you want to avoid model-release issues when selling to the client; regenerate any image with visible brand logos.

---

## Selling tip
Build the page, screenshot it on desktop + mobile, and pitch it to the company as "your customers google 'trädgårdsskötsel Solna' — right now they find your competitors." Their current online presence is only directory listings, so a real site is an easy upsell.
