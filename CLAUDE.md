# Vanguard Guild Website

## What this is
Static website for **Vanguard**, a World of Warcraft guild established in 2006 on Frostwolf. Hosted on GitHub Pages at `vanguard-guild.github.io`. The guild uses Roman military rank names and has a dark fantasy aesthetic.

## Architecture
- **Single file**: `index.html` — all HTML, CSS, and content in one file. No JavaScript.
- **No build process**: pure static HTML served directly.
- **No external dependencies** except Google Fonts (Cinzel + Crimson Text).

## Design system
- **Theme**: Dark background (#0a0a0a) with gold (#c9a84c) accents and warm beige text (#d4c9b0)
- **Fonts**: Cinzel (display serif, headings/UI) and Crimson Text (body serif)
- **CSS variables** defined in `:root` — use these, don't hardcode colors
- **Noise texture overlay** via SVG data URI on `body::before`

## Layout
- **Header**: "VANGUARD" / "EST. MMVI" / divider / tagline
- **CSS-only tab system** using hidden radio inputs + `:checked` sibling selectors (no JS)
  - Tabs: ABOUT | JOIN | ROLES | FAQ
  - Tab bar is `position: sticky` at top
  - Tab panels use `display: none/block` toggled by radio state
  - `fadeUp` animation on panel switch
- **About tab**: Guild intro paragraph + Guild Rules (Conduct, Activity, Grouping)
- **Join tab**: Recruitment CTA with in-game invite link
- **Roles tab**: Categorized (Leadership/Membership/Other) with `TITLE :: flavor text` format and hover tooltips
- **FAQ tab**: Q&A pairs
- **Footer**: Simple centered text

## Guild role hierarchy
Leadership: Legatus-Regent (GM), Praetor (Officer)
Membership: Centurion (Veteran), Initiate (Member), Recruit (New)
Other: Tribunus (Leadership alts), Evocatus (Memorial), Envoy (Guest/Discord), Paramour (Consort)

## Conventions
- All styling is embedded in `<style>` — no external CSS files
- Section headings use `h2` with Cinzel, 0.75rem, uppercase, gold, wide letter-spacing
- Do not use em-dashes (`—`) anywhere in content
- Roman/Latin naming convention for ranks and flavor text
- Keep the tone direct and human — avoid AI-sounding filler language
- Content should feel like it was written by a guild leader, not a marketing department

## Git
- Repo: `vanguard-guild/vanguard-guild.github.io`
- Branch: `main` (deploys to GitHub Pages automatically)
- `.claude/` directory is gitignored
