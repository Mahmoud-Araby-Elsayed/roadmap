# Mahmoud — Multi-Page Portfolio (Structure Only)

A four-page HTML-only website built to practice **semantic HTML structure**
across multiple pages. No CSS yet — styling is a deliberately separate
project. This one is about getting header, nav, main, sections, sidebars,
and footer right.

## Goals

- Learn how to build and link multiple pages on one site
- Structure every page semantically, not just visually
- Structure everything so styling can be added later without restructuring
- Add real SEO meta tags to every page

## Pages

| File | Page | Notable structure |
|---|---|---|
| `index.html` | Homepage | Hero, 3-column overview (Projects / Work Experience / Education), testimonials |
| `projects.html` | Projects | Two `<section>`s, each grouping multiple `<article>` project entries |
| `articles.html` | Articles | Blog-style `<article>` list + `<aside>` sidebar (categories, currently learning) |
| `contact.html` | Contact | Real `<form>` + `<address>` for contact details |

## Semantic elements used

| Element | Purpose | Where |
|---|---|---|
| `<header>` | Site branding + primary nav | Every page (identical block) |
| `<nav>` | Navigation links, with `aria-current="page"` marking the active page | Every page |
| `<main>` | The one unique content region per page | Every page |
| `<footer>` | Copyright | Every page (identical block) |
| `<section>` | Thematic grouping with its own heading | All pages |
| `<article>` | Self-contained content (would still make sense pulled out on its own) | Homepage (work entries), Projects (each project), Articles (each post) |
| `<aside>` | Genuinely secondary content, not required to understand the page | Articles page (sidebar) |
| `<div>` | Pure layout wrapper — no semantic meaning, just a future CSS hook | Homepage `.overview`, Articles `.page-layout` |
| `<figure>` / `<figcaption>` | Quote + attribution (used instead of `<cite>`, which is meant for work titles, not people) | Homepage testimonials |
| `<blockquote>` | Quoted text | Homepage testimonials |
| `<time datetime="">` | Machine-readable publish dates | Articles page |
| `<address>` | Contact info belonging to the page's author | Contact page |
| `<form>` / `<label>` / `<input>` / `<textarea>` | Accessible, properly-associated form controls | Contact page |

## SEO

Every page has its **own** `<title>`, meta description, canonical link,
Open Graph tags, and Twitter Card tags — not copy-pasted from the Homepage.
That's intentional; duplicate titles/descriptions across pages hurt SEO.

## Still placeholder — fill in before this goes live

- [ ] Homepage: real job title, company, education, and testimonial quotes
- [ ] Projects: `href="#"` links → real repo/live links once deployed
- [ ] Articles: excerpts only right now — full article pages aren't built yet
- [ ] Contact: real email, GitHub/LinkedIn links, and a form backend (e.g. Formspree, or your own endpoint) — the `action="#"` goes nowhere right now
- [ ] All pages: `canonical` and `og:url` use `https://your-domain.com/` — update once deployed

## What's next

Styling. The class names (`.site-header`, `.overview`, `.project`,
`.testimonial`, `.page-layout`, `.sidebar`, `.contact-form`, `.form-group`,
etc.) are already in place as CSS hooks — the next project can style this
without touching the HTML structure.