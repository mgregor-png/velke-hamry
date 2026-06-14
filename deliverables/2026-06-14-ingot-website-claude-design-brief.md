# INGOT website - Claude Design brief

Owner: Martin (co-owner, product). Drafted 2026-06-14. This is Phase 1 of the agreed plan: brand + content, then build.

Pairs with the visual reference: **`2026-06-14-ingot-styletile.png`** (the brand style tile). Source of the visual language: the Studio Reaktor architectural study (`inputs/Velké Hamry - nová studie.pdf`). Source copy: `2026-06-04-ingot-zmeny-a-finalni-texty.md` + `INGOT - souhrn uprav 6.6.pdf`.

The decision rule for every choice: **would this feel like the apartment itself - quietly designed, architectural, calm - or like a generic mountain-rental listing?** If it reads as "horská chata," Airbnb hard-sell, or fake-Nordic fjords, it is wrong.

---

## 0. The spine (read first)

INGOT is not a new brand built against Muhu. It is the elevation of **one apartment** into the design position its architecture already earns. The website is the one channel we fully control: it exists to win **direct bookings** (no OTA fee, best price) and to make a 28-45 design-conscious couple feel the level of the space before they arrive. Photo-led, minimal copy, confident. The building and the light are the subject.

**One page. CZ default with an EN toggle. Mobile-first.**

---

## 1. Paste-ready brief (for Claude Design / Stitch / Framer)

```
Build a single-page, mobile-first marketing + direct-booking website for a design apartment called INGOT, in Velké Hamry, Jizerské hory (Czech Republic). Bilingual: Czech default with an EN/CZ toggle in the nav that swaps all copy in place (no reload). Match the attached style tile (ingot-styletile.png).

WHAT IT IS
A ground-floor design apartment built to Studio Reaktor's "forged living ingot" concept: a black standing-seam metal facade, a warm pine (CLT) interior, its own terrace and front garden. The site sells the architecture and the feeling, and drives direct booking enquiries that bypass Booking/Airbnb fees.

VIBE
Editorial, architectural, calm, premium minimalism - the register of AESOP / MUJI / ARKET / Kinfolk, not a hotel site and not a hiking-cabin site. Lots of warm white space, big full-bleed photography, thin technical rules, small uppercase eyebrow labels. Confident and quiet. NOT "horská chata," NOT Airbnb-red, NOT fake-Nordic fjords, NOT a busy booking portal.

DESIGN SYSTEM (see tokens below)
Warm paper canvas, anthracite dark sections for rhythm, terracotta as the single CTA accent, sage as a secondary accent, warm pine for wood/number highlights. Space Grotesk for headings (bold, tight, uppercase eyebrows with wide tracking), Inter for body. Full-bleed photos, alternating light/dark sections, thin 1px rules, uppercase eyebrow + short hairline rule above each section title.

STRUCTURE (one scrolling page)
Sticky nav -> Hero -> O apartmánu (story, 3 columns) -> USP strip (dark) -> Galerie (grid + lightbox) -> Příběh (heritage + Studio Reaktor concept) -> Okolí (around, couples-oriented cards) -> Dostupnost (live Previo availability iframe) -> Rezervace (direct-booking benefits + enquiry form + "book now" Previo fallback) -> O nás (the two owners, personal) -> Footer (dark).

FUNCTION
Language toggle (CZ default, localStorage, sets <html lang>). Gallery lightbox. Live availability via embedded Previo iframe. Enquiry form posts to Formspree. "Book now" link opens the Previo booking engine filtered to this apartment. Smooth-scroll nav.
```

---

## 2. Design tokens

**Colour** (grounded in the study renders)

| Role | Hex |
|---|---|
| Paper / canvas (warm white) | `#F1EEE7` |
| Lifted paper / cards | `#E7E3D9` |
| Concrete / hairlines + secondary | `#BDB9AF` |
| Anthracite / dark sections + facade | `#2B2B28` |
| Ink / body text | `#23221F` |
| Pine / wood + number accents | `#C49A67` |
| Walnut / deep wood | `#7E6752` |
| **Terracotta / CTA + single accent** | `#BF562E` |
| Sage / secondary accent | `#7E8769` |

Rules: terracotta is reserved for the primary CTA, eyebrow labels, and one or two key accents per view - never a fill background. Alternate light paper sections with anthracite sections for rhythm (Hero photo, USP, Photography/Footer = dark). One accent per section, never terracotta + sage competing.

**Type**
- Headings + eyebrows + numbers: **Space Grotesk** (700 headings, 600 eyebrows). Eyebrows: 11px, uppercase, `letter-spacing .22em`, terracotta. Wordmark `INGOT`: uppercase, `letter-spacing .4em`.
- Body + UI: **Inter** (400/500), 16px, `line-height 1.6`.
- Both free on Google Fonts. Headings tight (`letter-spacing -.015em`); generous size jumps; never centre long text blocks (hero + section eyebrows can centre, body left).

**Layout**
- Max content width ~1100-1200px, generous 48px+ side padding on desktop, comfortable mobile gutters.
- Every section opens with: uppercase eyebrow (CZ · EN) + a short 1px hairline rule, then the H2.
- Full-bleed photography; thin rules as dividers; cards with 3px radius and hairline borders.

**Texture + motion**
- Minimal. No drop shadows as decoration (one soft offset on the sticker-style annotation tag is fine). Subtle fade-up on scroll is allowed; nothing cinematic.

**Illustration motif** (the part Martin liked from the study)
- The study's KONCEPT pages use grey axonometric massing blocks with terracotta + olive accent volumes, thin uppercase labels, technical line work. Reuse this as: the section divider into `Příběh`, a simple "pět ukovaných ingotů" massing graphic, and the `Okolí` mini-map styling. Keep it sparing - one or two diagram moments, not everywhere.

---

## 3. Voice

Confident, editorial, calm. Short declaratives. CZ is the base; EN is a true parallel (translate the meaning, not word-for-word). Never "horská chata," never fjord/Nordic cosplay, never Airbnb exclamation-mark sell. The space speaks; the copy gets out of the way.

---

## 4. Sections + paste-ready bilingual copy

Nav order (CZ / EN): **Apartmán** / Apartment · **Galerie** / Gallery · **Okolí** / Around · **Dostupnost** / Availability · **O nás** / About · CTA **Poptat termín** / Request dates. Toggle `[CZ | EN]` at the right of the nav.

### Hero (full-bleed: `terrace_hero.jpg` or `facade.jpg`)
- Eyebrow: `VELKÉ HAMRY · JIZERSKÉ HORY`
- H1: `INGOT`
- Tagline CZ: „Inspirováno Severem. Ukováno v Jizerkách." / EN: *"Inspired by the North. Forged in the Jizera Mountains."*
- Sub CZ: „Architektonicky ukovaný designový apartmán s vlastní terasou a předzahrádkou. Surový navenek, jemný uvnitř. 87 minut z Prahy."
- Sub EN: *"An architecturally forged design apartment with its own terrace and front garden. Raw on the outside, warm within. 87 minutes from Prague."*
- Buttons: **Poptat termín** / *Request dates* (primary, scrolls to form) · **Zobrazit dostupnost** / *See availability* (scrolls to calendar)

### O apartmánu / The apartment
- Eyebrow: `O APARTMÁNU · THE APARTMENT`
- H2 CZ: „Surový navenek, jemný uvnitř." / EN: *"Raw on the outside, warm within."*
- Perex CZ: „INGOT je přízemní designový apartmán postavený podle konceptu studia Reaktor jako jeden z ‚ukovaných obytných ingotů' - černá kovová fasáda, teplý borový interiér. Úroveň designu, která v Jizerkách není běžná."
- Perex EN: *"INGOT is a ground-floor design apartment built to Studio Reaktor's concept of 'forged living ingots' - a black metal facade, a warm pine interior. A level of design that is not common in these mountains."*
- Three columns:
  - **Architektura / Architecture** - CZ: „Ingotový tvar, černá kovová fasáda, industriální dědictví přímo z Velkých Hamrů - železné hamry od 13. století. Exteriér je identita, ne povrch." / EN: *"The ingot form, a black metal facade, industrial heritage straight from Velké Hamry - iron forges since the 13th century. The exterior is identity, not surface."*
  - **Interiér / Interior** - CZ: „Hřejivé borové dřevo (CLT konstrukce), šalvějové akcenty, kurátované umění a severská jednoduchost. Teplo a detail jako kontrast k surovému exteriéru." / EN: *"Warm pine (CLT construction), sage accents, curated art and Nordic simplicity. Warmth and detail as a counterpoint to the raw exterior."*
  - **Místo / The place** - CZ: „Vlastní terasa a předzahrádka s výhledem do lesa - místo na ranní kávu a večerní ticho, které většina apartmánů v Jizerkách nemá." / EN: *"A private terrace and front garden facing the forest - a place for morning coffee and evening quiet that most apartments here simply don't have."*

### USP strip (dark anthracite) - 6 tiles
Number in pine, label below. Drop "dětské hřiště" from the hero tiles (off-positioning for couples; keep it in full amenities only).

| CZ | EN |
|---|---|
| `87 min` z Prahy | `87 min` from Prague |
| `Terasa` vlastní terasa + předzahrádka | `Terrace` private terrace + garden |
| `Garáž` krytá garáž zdarma | `Garage` covered, free |
| `250 Mb/s` Wi-Fi, plně vybavená kuchyň | `250 Mb/s` Wi-Fi, full kitchen |
| `Ohniště` tři společná ohniště | `Fire pits` three shared |
| `Workout` venkovní workout zóna | `Workout` outdoor zone |

### Galerie / Gallery
- Eyebrow: `GALERIE · GALLERY` · H2 CZ: „Pohled dovnitř i ven." / EN: *"A look inside and out."*
- Responsive grid of the new pro photo set, click = lightbox. Lead with facade, terrace, pine interior, bedroom, fire pit at dusk, aerial, waterfall.

### Příběh / Story (heritage + concept - the merged "history + story of INGOT")
- Eyebrow: `PŘÍBĚH · STORY`
- H2 CZ: „Z hamrů. Pro klid." / EN: *"From the forges. For the quiet."*
- Part 1 - Velké Hamry (the history bit), CZ: „Jméno Velké Hamry nese dědictví železných hamrů, které tu bušily od 13. století. Industriální stopa, ne kulisa." / EN: *"The name Velké Hamry carries the heritage of the iron forges that rang here from the 13th century. An industrial trace, not a backdrop."*
- Part 2 - Studio Reaktor + the project, CZ: „V roce 2023 navrhlo studio Reaktor koncept ‚pěti ukovaných obytných ingotů' - domy jako kovové odlitky usazené do svahu. INGOT je jeden z nich, povýšený do podoby, kterou si jeho architektura zaslouží." / EN: *"In 2023 Studio Reaktor designed the concept of 'five forged living ingots' - houses like metal castings set into the slope. INGOT is one of them, raised to the form its architecture deserves."*
- Optional: the axonometric "five ingots" massing graphic here, one accent block highlighted (this one).

### Okolí / Around (repositioned for couples - keep best nature, add cafes/slow; drop stroller/kid framing)
- Eyebrow: `OKOLÍ · AROUND` · H2 CZ: „Jizerky a Krkonoše na dosah." / EN: *"The Jizera and Giant Mountains, within reach."*
- Cards (each: title, 1 line, optional Mapy.cz link):
  - **Protržená přehrada** - CZ: „Lesní stezka podél Bílé Desné k ruinám protržené přehrady. Klidná, atmosférická, ideální dopoledne." / EN: *"A forest trail along the Bílá Desná to the ruins of the burst dam. Calm, atmospheric, a perfect morning."*
  - **Vodopády / Waterfalls** - CZ: „Mumlavské vodopády a kaskády Jizery - krátké výlety za vodou a tichem." / EN: *"The Mumlava waterfalls and the Jizera cascades - short walks to water and quiet."*
  - **Rozhledna Štěpánka** - CZ: „Kamenná rozhledna nad lesy, panorama Jizerek i Krkonoš. Nejlepší za jasného večera." / EN: *"A stone lookout tower above the forests, panoramas of both ranges. Best on a clear evening."*
  - **Jizerka** - CZ: „Horská osada a rašeliniště s dřevěnými chodníky. Pomalá procházka, safírový potok." / EN: *"A mountain hamlet and peat bog with wooden boardwalks. A slow walk, a sapphire creek."*
  - **Kavárny a restaurace / Cafes & dining** - CZ: „Tipy na dobrou kávu a večeři v okolí - [doplnit konkrétní místa]." / EN: *"Where to find good coffee and dinner nearby - [add specific spots]."*
  - **Pomalé večery / Slow evenings** - CZ: „Vlastní terasa, ohniště pod hvězdami, sauna a wellness v dosahu - [ověřit]." / EN: *"Your own terrace, a fire pit under the stars, sauna and wellness within reach - [confirm]."*
- *Optional richer version later: port the interactive map + filters from the trip-planner app (`trip-planner.html`), restyled to INGOT and re-toned for couples.*

### Dostupnost / Availability
- Eyebrow: `DOSTUPNOST A CENY · AVAILABILITY & PRICES` · H2 CZ: „Volné termíny v reálném čase." / EN: *"Live availability."*
- Perex CZ: „Živý kalendář dostupnosti a cen přímo z rezervačního systému. Pro nejlepší cenu pošlete poptávku níže - vyřídíme ji napřímo." / EN: *"A live availability and price calendar straight from the booking system. For the best price, send an enquiry below - we handle it directly."*
- Embedded Previo iframe (see section 5). Caption CZ: „Kalendář zobrazuje živá data pro tento apartmán." / EN: *"Live data for this apartment."*

### Rezervace / Booking (split: benefits left, form right)
- Eyebrow: `REZERVACE · BOOK DIRECT` · H2 CZ: „Rezervujte napřímo." / EN: *"Book direct."*
- Three benefits (check marks):
  - CZ „**Nejlepší cena.** Bez prostředníka, bez příplatků portálů." / EN *"**Best price.** No middleman, no platform fees."*
  - CZ „**Přímý kontakt.** Rezervaci vyřídíme my, ne anonymní portál." / EN *"**Direct contact.** We handle your booking, not an anonymous portal."*
  - CZ „**Flexibilita.** Domluvíme příjezd, tipy na okolí i speciální přání." / EN *"**Flexibility.** We'll arrange arrival, local tips and special requests."*
- Form fields (labels CZ / EN): Příjezd/Arrival (date) · Odjezd/Departure (date) · Počet hostů/Guests (1-3) · Jméno/Name · E-mail · Telefon/Phone (optional) · Poznámka/Note (optional) · button **Odeslat poptávku** / *Send enquiry*.
- Microcopy under button CZ: „Odesláním nás kontaktujete napřímo. Žádná platba teď." / EN: *"This sends us a direct enquiry. No payment now."*
- Secondary line CZ: „Chcete rezervovat hned? Otevřít rezervační systém →" / EN: *"Prefer to book instantly? Open the booking system →"* (links to Previo booking engine, section 5).

### O nás / About us (personal - builds trust; FACTS TO CONFIRM with Martin)
- Eyebrow: `O NÁS · ABOUT US` · H2 CZ: „Dva majitelé, jeden apartmán." / EN: *"Two owners, one apartment."*
- Intro CZ: „INGOT vlastníme a staráme se o něj sami. Bez správcovské anonymity." / EN: *"We own INGOT and look after it ourselves. None of the management-company anonymity."*
- **Martin Smékal** - [role: ředitel / co-owner - CONFIRM exact title + one personal line].
- **Martin Gregor** - [product owner; léta v kreativních agenturách / years in creative agencies - CONFIRM phrasing; this is where the design sensibility comes from].
- *Tone: warm, brief, first names, one photo optional. Two short paragraphs, not CVs.*

### Footer (dark anthracite)
- Wordmark `INGOT` + tagline.
- Instagram: **@ingot_hamry**
- „Velké Hamry, Jizerské hory" / *"Velké Hamry, Jizera Mountains"*
- CZ: „Rezervujete přímo u nás, bez prostředníka. © 2026 INGOT" / EN: *"Book directly with us, no middleman. © 2026 INGOT"*

---

## 5. Functional integrations

**a) Live availability calendar (iframe):**
`https://booking.previo.cz/occupancy/?hotId=789961&currency=CZK&lang=cs&showRoomType=995241&redirectType=iframe`
(EN: swap `lang=en`. Toggle should switch the iframe `lang` param too.)

**b) "Book now" fallback (link/button to Previo booking engine, our unit only):**
`https://booking.previo.cz/?hotId=789961&currency=CZK&lang=cs&roomType=995241`

**c) Enquiry form -> Formspree:** `POST` to `https://formspree.io/f/xzdqyoeb` (live endpoint). Fields map to named inputs; include a hidden `_subject` ("INGOT - nová poptávka termínu"), and `_language`. Honeypot field (`_gotcha`) for spam. Note: first submission triggers a one-time Formspree confirmation email; add the final GH Pages domain under Allowed domains after deploy. Success state: inline confirmation (CZ „Díky, ozveme se co nejdřív." / EN *"Thanks, we'll be in touch shortly."*), no redirect.

**d) Language toggle:** `[CZ | EN]` in nav. Implementation: every translatable node carries `data-cs` / `data-en` (or a JS string map keyed by `data-i18n`); toggle swaps text, sets `<html lang>`, updates the Previo iframe `lang`, persists choice in `localStorage`, CZ default.

Key Previo IDs: hotId `789961` (MUHU Apartments), roomType `995241` (this apartment / INGOT), agency parId `5764805`. Manual booking entry at `agency.previo.app` (Martin holds access). Prices are pulled live by the iframe - do not hardcode prices on the page.

---

## 6. Assets

- **Photos (new pro set):** in `inputs/web/NEW fotky INGOT/` + `landing/assets/`. Best: `facade.jpg` (black standing-seam facade), `terrace_hero.jpg` (terrace + bike, sage bistro chairs, dappled light), pine-ceiling living/dining, bedroom, dusk fire pit, aerial of the development, waterfall. Style-tile crops in `deliverables/assets/styletile/`.
- **Style reference:** `2026-06-14-ingot-styletile.png` (this brand's tile) + study pages 1 / 11 (Inspirace) / 13 (Koncept) / 17 (render).
- **Fonts:** Space Grotesk + Inter (Google Fonts).
- A pro reshoot can upgrade later (styled interior + golden hour); current set is already strong.

## 7. Banned (kill on sight)
Airbnb-red and exclamation-mark sell · "horská chata" rustic-cabin tropes · fake-Nordic fjord/Viking cosplay · stock hospitality imagery (empty staged rooms, smiling-staff clipart) · busy OTA-style booking widgets crowding the page · drop-shadow/bevel/gradient decoration · centred walls of body text · more than one accent colour fighting per view · hardcoded prices.

## 8. Open items for Martin
1. ~~Formspree form ID + target email~~ - DONE: `https://formspree.io/f/xzdqyoeb`.
2. **O nás facts** - Smékal's exact title + one human line each; whether to include owner photos.
3. **Okolí specifics** - real cafe/restaurant picks; confirm sauna/wellness nearby; OK to port the trip-planner map later?
4. Confirm the 6 USP tiles (esp. dropping the playground from the hero set).
5. EN tagline final call: "Inspired by the North. Forged in the Jizera Mountains." (current) vs a shorter "Forged in the North."
6. Deploy target: `mgregor-png/velke-hamry` GH Pages (same repo as positioning), clean URL.
