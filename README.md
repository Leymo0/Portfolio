# leymo's portfolio

Plain HTML/CSS, no build step, no framework. Just open `index.html` in a browser to preview it locally.

## Structure

```
index.html                       home page (the crafting-grid nav)
style.css                        shared styles for every page
projects/mc-override-studio.html project page
projects/lol-draft-tool.html     project page
tools/mc-override-studio.html    the actual working tool, linked from its project page
```

To add a new project:
1. Copy `projects/lol-draft-tool.html` as a starting template.
2. Fill in its content.
3. On `index.html`, turn one of the `<div class="slot empty"></div>` cells in the crafting grid into
   an `<a class="slot filled" href="projects/your-page.html" style="--slot-color:var(--gold); --slot-glow:var(--gold-glow)">` (copy the icon markup pattern from an existing filled slot, or swap in your own SVG).

## Things marked TODO

A few spots are intentionally left as placeholders — search for `TODO(leymo)` in the HTML files:
- Footer GitHub/email links on every page (currently `href="#"`)
- Screenshots/demo links on the League draft tool page (written from memory of our chats — the
  actual stack/details weren't specified, so fill those in and I can tighten the copy)

## Deploying it for free

**GitHub Pages (recommended, free, your own repo):**
1. Create a new GitHub repo (e.g. `portfolio`).
2. Push this whole folder to it.
3. In the repo, go to Settings → Pages → set source to the `main` branch, root folder.
4. Your site goes live at `https://<your-username>.github.io/portfolio/` within a minute or two.

**Netlify (also free, drag-and-drop, no git needed):**
1. Go to app.netlify.com → "Add new site" → "Deploy manually".
2. Drag this whole folder into the upload box.
3. It gives you a live URL immediately; you can rename it or attach a custom domain later.

Both options work fine since this is a fully static site — no server, no database, nothing to configure.
