# Documentation project instructions

## About this project

- This is the internal Mintlify documentation site for the **OPBG Clients Portal**
- The product source code lives in the separate `opbg-clients` repository
- This repository is the publishing target for the docs site
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

- Use `dashboard` for a portal-connected JobTread job
- Use `draw` or `invoice draw` for the standard billing workflow
- Use `sign-off package` for the 40-40-20 workflow
- Use `client` for external viewers
- Use `superintendent` for internal non-admin users
- Use `vendor bill` for subcontractor or supplier cost records
- Use `customer invoice` for the client-facing invoice created in JobTread
- Use `Statement of Values` or `SOV` for the contract-value breakdown
- Use `VENDOR NOT LET` exactly in all caps when describing approved scope without a PO

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise and operational
- Prefer Feynman-style explanations: explain the behavior simply first, then name the code or table behind it
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Favor tables when documenting permissions, workflows, or source-of-truth ownership
- Treat the app code as the final authority if older markdown disagrees

## Content boundaries

- This site is internal-first, so internal admin behavior and sensitive workflow rules should be documented
- Document real behavior for restricted cost codes, share links, approval side effects, and 40-40-20 mode
- Keep technical reference operational rather than exhaustive
- Do not mirror every hook or utility file unless it changes user-visible behavior or system ownership
- Do not treat `opbg-clients/docs/CLAUDE.md` as current authority for product behavior
- When describing the system, prefer these source areas in order:
  1. `src/App.tsx` and routed pages
  2. `src/hooks/**`
  3. `supabase/functions/**`
  4. Existing markdown in `opbg-clients/docs/**`
