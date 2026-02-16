# GIS & Geography Portfolio

A responsive, dark-themed portfolio site for TCU geography and GIS student work. Built with semantic HTML, CSS, and minimal JavaScript.

## Structure

- **index.html** — Home with hero and featured project cards
- **about.html** — Education, focus areas, and skills
- **projects.html** — Full project grid (modular; add cards as needed)
- **contact.html** — Contact links (update email and LinkedIn URL)
- **css/styles.css** — All styles (variables, layout, components)
- **js/main.js** — Mobile menu toggle and header scroll state

## Adding a New Project

1. Open **projects.html** and find the `project-grid` div.
2. Copy one full `<article class="project-card">...</article>` block.
3. Paste it inside the grid (before the comment block).
4. Set a unique `id` on the article (e.g. `id="project-my-map"`).
5. Use the same `id` in the card link `href` and, if you feature it on the home page, in **index.html** links (e.g. `projects.html#project-my-map`).
6. For a real image: replace the `project-card-placeholder` div with:
   ```html
   <img src="images/your-image.jpg" alt="Brief description" class="project-card-image">
   ```
   Add images to an `images/` folder.

## Updating Contact Info

Edit **contact.html** and replace:

- `your.email@tcu.edu` in the `href` of the email link
- `https://www.linkedin.com/in/yourprofile` with your LinkedIn profile URL

## Running Locally

Open **index.html** in a browser, or use a simple local server:

```bash
# Python
python3 -m http.server 8000

# Node (npx)
npx serve
```

Then visit `http://localhost:8000` (or the port shown).

## Design Notes

- **Colors:** Dark background (`#0a0a0f`), deep purple accents (`#7c5cff`). Override in `:root` in `css/styles.css` if needed.
- **Accessibility:** Semantic headings, `aria-current` on nav, focus styles, and `prefers-reduced-motion` support. Ensure contrast when changing colors.
- **Expandable:** Project grid uses `auto-fill` and `minmax(320px, 1fr)` so new cards flow in without layout changes.
