# Kerno Webflow Animations

Self-contained HTML embeds for the Kerno website. Each file is a standalone Webflow Custom Code embed — no external dependencies, no build step required.

## Structure

```
embeds/
  kerno-cli.html          — CLI install & onboarding demo
  <next-animation>.html   — ...
```

## How to use

1. Open the embed file in a browser to preview it.
2. Copy the entire file contents.
3. Paste into a Webflow **Embed** element's HTML editor.

## Conventions

- Each embed is a **single HTML file** containing `<style>`, markup, and `<script>` — all inline.
- No external JS libraries. Google Fonts `@import` is allowed.
- The outermost element uses a scoped class (e.g. `.kerno-cli-demo`) to avoid style leakage.
- All animations auto-play on load and include a **↻ Replay** button in the title bar.
- Responsive: include a `@media (max-width: 480px)` block for mobile adjustments.

## Adding a new animation

1. Duplicate the closest existing embed in `embeds/`.
2. Rename it to something descriptive (e.g. `kerno-agent-run.html`).
3. Update the scoped class name throughout.
4. Build the animation, then commit.
