# @sustin/tokens

Shared design tokens (CSS custom properties) for the Sust.in sites: i5forum.org, i5academy.org and later i5benchmark.com. One file, no build step.

## Use

Install from this repository at a tagged version (not published to a registry):

```bash
pnpm add github:sustin-git/sustin-tokens#v0.1.1
# or
npm install github:sustin-git/sustin-tokens#v0.1.1
```

Import it before the site's own tokens:

```css
@import '@sustin/tokens';
@import './site-tokens.css'; /* site-only tokens and overrides */
```

## What is in it

| Group | Tokens |
| --- | --- |
| Surfaces and text | `--bg`, `--surface`, `--surface-2`, `--ink`, `--ink-2`, `--ink-3`, `--line` |
| Brand | `--indigo`, `--blue`, `--cyan`, `--lilac`, `--violet`, `--deep` |
| States | `--error`, `--success`, `--notice`, `--focus`, `--link` |
| Gradients | `--grad`, `--grad-solid`, `--grad-solid-hover`, `--grad-on-dark`, `--grad-text` |
| Type | `--font-head`, `--font-sans`, `--font-mono`, `--font-cjk`, `--fs-*`, `--track-head`, `--track-hero`, `--measure` |
| Shape and spacing | `--r-xl`, `--r-lg`, `--r-md`, `--r-pill`, `--panel-gap`, `--pad-block`, `--pad-block-tight`, `--pad-inline` |
| Motion | `--ease-out`, `--ease-expo` |

Fonts are named, not shipped. Each site self-hosts Space Grotesk, Geist and Geist Mono (all SIL OFL), e.g. from `@fontsource-variable/*`.

## Themes

- Light is the default.
- Dark applies when the OS prefers dark and `<html>` is not set to `data-theme="light"`, or on any element with `data-theme="dark"`.
- `data-theme="light"` and `data-theme="dark"` work on any element, so a section can flip theme inside a page.
- `.on-dark` styles a deep-indigo panel inside either theme.

## Not in here

Site-specific tokens stay with the site: i5Forum's glass, aurora, navigation tiles and layout sizes; i5Academy's five dimension colours.

## Changing a token

1. Change it here, bump the version in `package.json`, tag `vX.Y.Z`.
2. Update the dependency in each site and check both light and dark themes there.

Values were taken from i5summit `src/styles/tokens.css` at commit 6f855c2 (12 November 2026).

## Licence

MIT, see [LICENSE](LICENSE). Copyright (c) 2026 Sustainable Intelligence ASBL.
