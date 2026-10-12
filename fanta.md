# Project design specification

This project-local specification records design intent. Update it as the brief becomes concrete. Direct user instructions, AGENTS.md and the selected agent mode take precedence. Preserve existing work and use this project’s actual foundations rather than assuming a generic style.

## Product and audience
- Product purpose and key task: travel marketplace home ("estancia", original brand) for discovering experiences and stays; layout cloned from a reference booking site.
- Screens: Desktop — Inicio (1440×1180) and Mobile — Inicio (390×940, fixed bottom tab bar). Spanish (es-ES) copy.
- Choose a coherent visual direction suited to the product; maintain established brand decisions.

## Foundations
- Define semantic palette roles such as surface, text, muted text, border, accent and status; check readable contrast.
- Define typography roles such as display, heading, body, label and caption. Preserve existing font choices when present.
- Use a consistent spacing scale with explicit container padding and gaps. Record chosen token values here as the design evolves.
- Theme collection (Light): brand #FF385C, surface #FFFFFF, surface-alt #F7F7F7, surface-chip #F2F2F2, text #222222, text-muted #6A6A6A, border #DDDDDD, badge #F2F2F2E6.
- Type: Inter. Section title 22/600 desktop, 18/600 mobile; card title 14/600; meta 12 and 11.5 muted; labels 13/500.
- Spacing: desktop margins 80, card gap 15, tile gap 10; mobile margins 20, carousel gap 12–14. Radii: media 16, pills fully rounded.

## Layout and alignment
- Buttons: use a horizontal auto-layout frame, intentional padding/gap and requested alignment. Auto-width labels hug their text; minimum control dimensions belong to the container. Check label/icon alignment in screenshots.
- Cards: use nested rows/columns, stretch or fill children deliberately, and let auto-height paragraphs wrap at their assigned width. Hug content height where appropriate; fixed height requires a deliberate clipping/overflow decision.
- Avoid per-child position nudges to compensate for incorrect container sizing. Verify narrow and wide representative sizes for wrapping, clipping and stable alignment.

## Reusable design system
- Inspect existing components, collections, modes, variable values and bindings first.
- Create semantic foundation variables, then reusable component masters, bind applicable properties to variables and compose screens from instances. Keep stable identities and reuse existing tokens/components.
- Record component roles, states, variants, and chosen theme modes here. Verify that mode changes resolve the intended bound values.
- Components: Experience Card (media + badge + heart, title/host/price; reused for stays with overrides), Category Tile (media + label). Instances carry per-card text and media overrides. Theme mode: Light.

## Images and vectors
- Photography: 23 Fanta Gen AI images (fanta-image-1, 2048² WebP) in one editorial travel style — natural light, candid, no text/logos. Set as image fills on the card/tile Media layers via instance overrides; master defaults are the flamenco and Rutas culturales photos.
- Category icons: 4 Fanta Gen AI SVGs (replicate-recraft-v4.1-svg) in a flat-shaded style, rendered to 512px transparent PNGs and used as image fills (mode fit) on the 36px icon frames.
- Reuse supplied project assets. Offer generated imagery or SVG artwork when it materially improves the requested design and the brief leaves it open; ask about intent before preparing a generation request.
- Generation preparation opens the existing composer for review. It does not submit a paid request or promise an unavailable model.

## Acceptance checks
- Save complete valid FNX documents and inspect parser diagnostics.
- Verify screenshots of changed frames at representative sizes; fix misalignment, overlaps, clipping, typography and contrast before reporting completion.
- Check component reuse and bound variable modes. Preserve user content and existing project rules.
