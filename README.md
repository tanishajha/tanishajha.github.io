# tanisha.jha — personal portfolio

[![Live site](https://img.shields.io/badge/live-tanishajha.github.io-d9663d?style=flat&labelColor=15191c)](https://tanishajha.github.io)
[![No build step](https://img.shields.io/badge/build-none-d9663d?style=flat&labelColor=15191c)](#run-it-locally)
[![Vanilla JS](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-d9663d?style=flat&labelColor=15191c)](#tech-stack)

My personal portfolio: a dark, multipage site for my projects, experience, skills and résumé. I'm a B.Tech Automation & Robotics student (GGSIPU, Delhi) who builds backend, systems and automation software, from PLC logic to workflow schedulers.

The whole site is one static file with no framework and no dependencies.

**Live:** https://tanishajha.github.io

## Pages

| Page | What's on it |
| --- | --- |
| Home | Intro, selected projects, what I do, current focus |
| Projects | Case-study style write-ups with tech tags and metric badges |
| Work | Experience, education, leadership, achievements, certifications |
| About | Background, current focus and the tools I use |
| Résumé | Condensed résumé with a print-to-PDF button |
| Contact | Email, profiles and a contact form |

## Features

- **Command palette search.** Press `Ctrl K` (or `Cmd K`, or `/`) to search pages, projects, skills, certifications and links. Arrow keys move, `Enter` opens, `Esc` closes.
- **Custom cursor.** A dot with a trailing ring that changes size over links, text, inputs and while clicking. It only appears on devices with a mouse.
- **Interactive background.** A canvas network of drifting nodes that reacts to the pointer.
- **Motion with restraint.** Staggered hero entrance, a terminal that types itself, scroll reveals, animated SVG project art, a logo that draws itself on load and a scroll-progress bar.
- **Hash-based routing.** Pages switch instantly with no reload, and it works on any static host without server configuration.
- **Responsive and accessible.** Adapts to phones, has visible keyboard focus and a skip link, and turns motion off when the visitor has `prefers-reduced-motion` set.
- **Print-ready résumé.** A print stylesheet hides the navigation so the Résumé page saves cleanly as a PDF.

## Tech stack

- HTML, CSS and vanilla JavaScript in a single `index.html`
- Fonts: [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) and [JetBrains Mono](https://www.jetbrains.com/lp/mono/), loaded from Google Fonts
- Hosting: GitHub Pages

## Project structure

```
.
├── index.html      # the entire site: markup, styles, content and scripts
├── portrait.jpg    # optional, shown automatically on the About page
├── *.png           # optional project screenshots
└── README.md
```

## Run it locally

Open `index.html` in a browser. The fonts need an internet connection.

To serve it the way GitHub Pages does:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Customize it

Everything you'd normally edit sits at the top of the `<script>` block in `index.html`.

| To change | Edit |
| --- | --- |
| Projects | the `P` list (title, year, description, tech tags, links) |
| Metric badges under projects | the `BD` object, keyed by project `id` |
| Jobs, leadership, achievements | `J`, `POS` and `ACH` |
| Certifications and skills | `CERT` and `T` |
| Colors | the CSS variables in `:root` (`--ac` is the orange accent) |

The search index is built from these same lists, so new content becomes searchable automatically.

**Images.** Add a screenshot to a project with `img:'taskflow.png'` in its entry. Without it, the site shows a small animated illustration. Put a file named `portrait.jpg` next to `index.html` to show a photo on the About page.

## Deploy

1. Create a public repository named `<username>.github.io`.
2. Upload `index.html` (and any images) to the root.
3. In **Settings → Pages**, choose **Deploy from a branch**, then `main` and `/ (root)`.
4. The site goes live at `https://<username>.github.io` in a minute or two.

## Notes

- The contact form opens your email app with the message filled in. There is no backend.
- Visual design inspired by [sunnypatel.net](https://www.sunnypatel.net/).

## License

The code is available under the MIT License. The text, projects and résumé content are © 2026 Tanisha Jha.
