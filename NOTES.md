# Christ For All Nation Worship Centre — build notes

## Job type
Lovable rebuild (CLAUDE.md §0 case B). Old site: `christforallnations.lovable.app`.

## Phase 1 (v1)
Generated via `generate.py`, palette `royal`, theme "african worship nations gathered".
Hero: "Christ for / all nations." Scripture: Mark 16:15.

## Phase 2 (refine — this pass)
Screenshots supplied in `/home/wdf-websites/screenshot/` (flat folder, not per-church —
had to identify the right 6 of 9 by content; the other 3 were a different church, "Centre
of Faith Bible Church").

**Logo:** not present in `Site Logoes/` (checked all 11 files — none matched). Cropped
cleanly from the largest clean occurrence in the screenshots (hero card, `13.47.38.png`),
trimmed and upscaled 4x with Lanczos + unsharp → `assets/img/logo.png`. Real crest: navy
globe + dove + maroon cross, three figures, "CHRIST / FOR ALL NATION / WORSHIP CENTER"
wordmark. Used in nav (white chip) and footer (white chip) — matches how the church's own
site displays it (white card against their navy hero).

**Leadership photo:** real photo of the two pastors, also cropped from `13.47.38.png`
(the only screenshot with a clean, uncropped-by-scroll view) → `assets/img/leadership.jpg`.
Used in new Leadership section.

**Palette:** old site is navy blue + maroon/crimson (crest sampled to ~#18377A navy,
~#6D1D2E maroon), not the template's navy+gold. Kept the `ink/ash/coal` dark stage and
`ember` blue accent as-is; retuned `blaze` → `#1B3A78` (real navy) and `gold` → `#D2536A`
(a brightened, WCAG-AA-legible tint of the real maroon — token still named `gold` in the
CSS/Tailwind config to avoid a risky mass rename, but it now holds the crimson brand
color, not literal gold). Updated in `index.html` tailwind config, `css/style.css`
(`:root` vars + literal rgba values), and `js/main.js` (ember-field particle palette).

**Real content carried across** (from the old site's Home/Vision/Mission/Leadership/Contact
pages):
- New **Vision** section: Matthew 28:20 + Isaiah 43:19 verse cards (their actual vision
  anchors — kept the original Mark 16:15 pinned-scripture moment too, as a second, distinct
  cinematic beat, not a replacement).
- "What to expect" → real **Mission** section: Preaching / Teaching / Witnessing /
  Training / Caring, with their exact one-line descriptions and tagline.
- New **Leadership** section: real photo + their real copy about the pastors' heart for
  the nations, naming Pastor Tshililo Hilton Dakalo (his wife/co-pastor is shown but
  unnamed in the source — did not invent a name for her).
- Real phone **+27 82 976 4039** now used everywhere (nav-adjacent CTA, Times & Place,
  closing CTA, footer) — replaced the template's fake `+27000000000`.

**Deliberately NOT invented:**
- Service times — the old site shows none (unlike "Centre of Faith Bible Church," a
  different church whose screenshot was in the same batch and does list times — do not
  confuse the two). Removed the template's fabricated Sun 09:00 / Wed 18:00 / Fri 18:30
  and replaced with an honest "we're finalising our schedule, call us" note + the real
  phone number.
- Street address — never shown in any screenshot. Left at city/province level
  (Thohoyandou, Limpopo) only, which is real (from the brief), not invented. Map embed is
  a city-level search, not a fabricated pin.
- Specific ministries list (Prayer & Intercession / Worship & Praise / Youth on Fire /
  Community Outreach) — this is still the generic v1 placeholder set; the old site's
  "Ministries" nav item had no captured page content. Not a factual claim like
  times/address/phone, so left as-is rather than blocking the refine — flagged to the
  operator to supply real ministry names if they have them.

## Open items for the operator
- Real street address, if any.
- Real service times, if any (site currently has none listed anywhere — shows a "call to
  confirm" note instead).
- Specific ministry names/programs, if they want something more specific than the generic
  four categories currently shown.
