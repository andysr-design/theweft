# The Weft — Design System v0.4

**Scope:** theweft.net and its projects.
**Status:** Source of truth. The live site does not yet reflect it — build to this, not from what's there.

## How to use this document

If you're Claude Design, Claude Code, or another agent prototyping for this project: apply the rules below directly, without asking, whenever one covers the case in front of you. Andy leads conceptual direction — your job is to execute and pressure-test inside these constraints, not propose alternative visual languages, invent new taxonomy, or generate options he hasn't asked for. Only flag something when no rule below resolves it.

This covers visual and content patterns only — typography, colour, voice, component behaviour. It does not cover infrastructure or hosting.

Two things worth knowing before you start:
- The case study system is still being designed by Andy himself. If a prototype touches it, flag rather than invent a template — public-sector, influence-based outcomes shouldn't be forced into an artefact-first format.
- No photography, anywhere, except case-study screenshots (S1–S3). Don't add imagery to solve a layout problem.

## Changelog

- **v0.4** — Tested by handing v0.3 cold to Claude Design and prompting for a homepage. Two real ambiguities surfaced and resolved: L7 had no concrete anchor and defaulted to a restrained, regular-weight headline — kept that restraint rather than forcing "oversized bold," since it read as more deliberate. L4/L6's boundary between chrome and content wasn't accounting for link-wrapped content tiles (project cards) — widened L6 to cover any content acting as a single clickable unit, not just nav/buttons/tags. Ink, paper, and orange are now confirmed hex values across light and dark modes, tested in a real working build rather than a single component.
- **v0.3** — Logged after first two component tests (signal card, Plain Jane audit). Added L6–L8 (interactive chrome pill treatment, hero headline scale, wordmark exception), C4–C7 (orange as the single action accent, cool off-white background, dark-mode inversion, scoped severity palette for the editor). Confirmed Arial and the 66-character measure against real precedent. Flagged open gaps: exact hex for off-white/Signals themes/editor severity colours, and Plain Jane's toolbar needs rebuilding to match L6.
- **v0.2** — Restructured from prose if/then into condition/action/reason tables for faster machine and human scanning. Scope narrowed to theweft.net and its projects; reference citations removed from the body.
- **v0.1** — First draft. Voice (GOV.UK plain English), visual language (Rams-influenced calm-minimal), no-photography sustainability constraint, Arial typography logic, initial colour and cross-project scope structure.

**Format note:** every rule is condition → action → reason, one row, no narrative glue. This is a rulebook, not an essay. If a rule is ambiguous in a real build, that's a gap in the rule, not a reading error — flag it and we patch it.

**Tie-breaker:** if two rules conflict, legibility and calm outrank expressiveness.

---

## 1. Voice & content

| ID | If | Then | Because |
|---|---|---|---|
| V1 | writing any sentence | keep one idea per sentence, one idea per paragraph | short sentences carry more attention |
| V2 | a plainer word exists | use it over the formal/technical one | plainness reads as competence to this audience, jargon doesn't |
| V3 | describing an action | use active voice, name who's doing it | passive voice hides responsibility |
| V4 | writing a heading or button | put the verb or outcome first | people scan; first two words carry the weight |
| V5 | writing a case study or portfolio piece | state the conclusion before the evidence | matches how a hiring manager actually reads |
| V6 | a hedge or self-deprecating qualifier appears | cut it | direct, not apologetic, is the established voice |

## 2. Visual language

| ID | If | Then | Because |
|---|---|---|---|
| L1 | an element doesn't communicate content or enable an action | remove it | "as little design as possible" |
| L2 | choosing between a visual flourish and whitespace | choose whitespace | calm is what's absent as much as what's present |
| L3 | a page needs visual hierarchy | build it with type size, weight, spacing | typographic hierarchy travels across all three projects without a matching icon set |
| L4 | a component could have a border/shadow/fill or not | default to not, unless it's interactive chrome (see L6) | borders and shadows date fastest; whitespace and alignment don't |
| L5 | setting density for signals / blog / editor | signals densest, editor closest to blank page, blog between | one visual language, three different reading tasks |
| L6 | building interactive chrome — nav, buttons, tag pills, *and any content tile that's wrapped as a single link (e.g. a project card)* | use a filled, glass-blur "pill/card" treatment — subtle translucent fill, soft border, hover lift and shadow; nav can be sticky/floating | a whole card acting as a link is a control, not passive content — it earns the same affordance as a button (see L4) |
| L7 | setting a hero-level statement headline | keep it restrained — modest size (~39px), regular weight, tight line-height (1.2), against the paper background | scale alone isn't the point; a quiet, confident statement reads as more deliberate than a shouted one, and matches the calm-minimal principle (L1–L2) more than an oversized headline does |
| L8 | setting an app or product name (masthead, wordmark) | keep it regular weight, modest size — same restraint as L7, distinct context | a product name is chrome, not a statement; both L7 and L8 now share the same quiet register, just applied to different content |

## 3. No photography — sustainability

| ID | If | Then | Because |
|---|---|---|---|
| S1 | a page needs a visual anchor | use typography, layout, or plain SVG — never a photo | images are the heaviest asset type; cutting them is the single biggest carbon lever |
| S2 | an icon is needed | use inline SVG, not an icon font or image file | keeps page weight low, consistent with S1 |
| S3 | a case study needs to show real work | screenshot is the one allowed exception — compress, correct size, lazy-load | rule is "no photography," not "no evidence"; every exception is a conscious trade, not a default |
| S4 | the AI-built-while-minimising-footprint tension comes up in copy | name it directly, don't smooth it over | more credible than pretending it isn't there, and matches the direct voice (V6) |

## 4. Typography
*Typeface: Arial.*

| ID | If | Then | Because |
|---|---|---|---|
| T1 | text is body copy | minimum 16px desktop, 18px mobile | floor for comfortable reading, not a target to hover near |
| T2 | text is a caption/footnote/short UI label | may go below 16px | fine for scanning, never for continuous reading |
| T3 | setting a line of running text | measure 45–90 characters, ~66 ideal for long-form | most reliable readability lever, costs nothing |
| T4 | text block is a paragraph or more | line-height ≥1.5 | long text needs vertical air to stay readable |
| T5 | text is a heading or 1–2 sentence intro | line-height 1.0–1.35 | short text doesn't need line-to-line tracking room |
| T6 | separating paragraphs | whitespace (≥1em), not indentation | standard web convention |
| T7 | choosing text alignment | left-align, never justify | justified text breaks word-spacing evenness, fights L1–L4 |
| T8 | heading is large (~24px+) | tighten letterspacing slightly | large type reads fine tight |
| T9 | text is uppercase or small caps | loosen letterspacing | uppercase needs room or it looks cramped |

## 5. Colour

| ID | If | Then | Because |
|---|---|---|---|
| C1 | colour is used at all | it must signal something (theme, state, action) | a colour with no job is noise (L1) |
| C2 | the four Signals themes need distinguishing | small local colour system, scoped to Signals only | gives the themes a real job without colour bleeding into the rest of the system |
| C3 | anywhere outside Signals' theme system | near-monochrome (ink on paper) + one accent — orange | one consistent accent keeps the shared system calm and legible as a signal in its own right |
| C4 | an element is interactive or actionable — button, active nav state, link, tag pill | use the orange accent | gives the accent a single, consistent job: action and interaction, nowhere else |
| C5 | setting the page background in light mode | cool off-white `#FBFAF9`, ink `#20241F` | confirmed from a full working build — crisp contrast without the starkness of pure white |
| C6 | the site offers a light/dark toggle | invert to paper `#1B1E1A`, ink `#F4F2ED` in dark mode; keep the orange accent (`#D9491F`) unchanged across both | confirmed from a full working build with both modes wired up; the accent's one job (C4) shouldn't change with mode — only the surface it sits on does |
| C7 | a tool needs to mark up content itself — severity, grammatical pattern, analysis state (e.g. the editor's hard-to-read or passive-voice flags) | use a small scoped palette local to that tool, never the orange accent | analysis markup is telling you something about the content, not offering a control — conflating it with the action accent breaks C4's one-job rule |

*Open: Signals' four-theme palette and the editor's C7 severity palette are still unresolved. Ink, paper, and orange are now confirmed across light and dark modes — no longer open.*

## 6. Cross-project scope

| | Shared everywhere | Local to one project |
|---|---|---|
| Typeface | Arial + all of Section 4 | — |
| Voice | All of Section 1 | — |
| Photography | S1–S4, no exceptions | — |
| Colour | C1, C3–C6 (orange = action, everywhere) | C2 — Signals' four-theme palette; C7 — editor's severity/analysis palette |
| Density | L5 baseline | exact values per project |

---

## Next steps

1. **Rebuild Plain Jane's toolbar to L6** — it currently predates the glass-pill decision, and L6 now covers content-tile cards too, so the toolbar and any content cards in the editor should both be checked against it.
2. **Resolve remaining open colour values** — Signals' four themes (C2), editor severity palette (C7) — against a real build.
3. **Publish to GitHub** — as a callable reference document for Claude to draw on in future project chats/experiments, alongside the Notion source of truth. Steps not yet worked out — starting fresh in a new chat.
4. **Publishing to the site** — Notion as source of truth with a changelog, mirrored to a public page in the Work section once tested. Not yet built.

