# Cursor Landing Page  UI Recreate

A static HTML/CSS recreation of the [Cursor](https://cursor.com) homepage. Built with vanilla HTML and CSS only (no frameworks).

---

## Sections Recreated

| Section | Description |
|--------|-------------|
| **Header** | Fixed top bar with Cursor logo, nav links (Features, Enterprise, Pricing, Resources), and CTAs (Contact, Sign in, Download). |
| **Hero** | Main headline (“Built to make you extraordinarily productive…”), primary Download CTA, and editor showcase with a **custom-built Cursor UI mock** (window chrome, In Progress / Ready for Review sidebar, code area) not screenshot. |
| **Logos** | Horizontal strip of company logos (OpenAI, Linear, Datadog, NVIDIA, Figma, Ramp, Adobe, etc.). |
| **Agent IDE** | “Agent turns ideas into code” feature card with copy and local asset (`public/agent.png`). |
| **Tab** | “Magically accurate autocomplete” section for Cursor Tab, with text and image (`public/tab.png`). |
| **Pull** | “In every tool, at every step” (GitHub PRs, Slack, terminal) with local image (`public/pull.png`). |
| **Testimonials** | “The new way to build software” heading and grid of quote cards (Diana Hu, Jensen Huang, Andrej Karpathy, Patrick Collison, shadcn, Greg Brockman). |
| **Frontier** | “Stay on the frontier” with three cards: Use the best model, Codebase understanding, Develop enduring software. Uses local images `frontier-one.png`, `frontier-two.png`, `frontier-three.png`. |
| **Changelog** | Changelog list (e.g. 2.4, CLI entries, 2.3) with dates and “See what’s new” link. |
| **Join us** | Careers/research CTA (“Cursor is an applied research team…”) with photo. |
| **Recent highlights** | Blog-style cards (Cursor 2.0, Tab RL, MoE kernels) and “View more posts” link. |
| **Try Cursor now** | Final CTA block with “Download for Windows”. |
| **Footer** | Product, Resources, Company, Legal, Connect link groups; copyright and SOC 2 note. |

---

## Fonts

- **Primary:** **Cursor Gothic** (Cursor’s marketing font)  
  - Loaded via `@font-face` from:  
    `https://cursor.com/marketing-static/_next/static/media/CursorGothic_Regular-s.p.a361088d.woff2`  
  - Format: `woff2`, `font-display: swap`.

- **Fallback stack:**  
  `system-ui`, `-apple-system`, `BlinkMacSystemFont`, `"Segoe UI"`, `Roboto`, `sans-serif`

---

## Colors (CSS Variables)

Defined in `:root` in `style.css`:

| Variable | Value | Usage |
|----------|--------|--------|
| `--color-bg` | `#14120b` | Page background |
| `--color-fg` | `#edecec` | Primary text / buttons |
| `--color-fg-02` | `#d7d6d5` | Secondary text, hover |
| `--color-nav-li` | `#d7d6d5c0` | Nav link (with alpha) |
| `--color-card-hex` | `#1b1913` | Card background |
| `--color-card-01-hex` | `#1d1b15` | Card variant |
| `--color-card-02-hex` | `#201e18` | Card / hover |
| `--color-card-03-hex` | `#26241e` | Card darker |
| `--color-card-04-hex` | `#2b2923` | Borders / inputs |
| `--color-card-hover` | `#201e18` | Hover state |
| `--color-border-02` | `#edecec1a` | Subtle borders |
| `--color-text-sec` | `#edecec99` | Muted text |
| `--color-add-green` | `#1f8a65` | Positive / add (e.g. diff) |
| `--color-add-red` | `#cf2d56` | Negative / remove |

Overall palette is dark (near-black `#14120b`) with light gray/off-white text (`#edecec`, `#d7d6d5`) and warm gray card tones.

---

## Project Structure

```
Cursor-UI-HTML-CSS/
├── index.html      # Single-page markup
├── style.css       # All styles and variables
├── README.md       # This file
└── public/         # Local images
    ├── agent.png
    ├── frontier-one.png
    ├── frontier-two.png
    ├── frontier-three.png
    ├── pull.png
    └── tab.png
```

Some images (hero background, logos, avatars, blog/changelog assets) are still loaded from Cursor’s CDN or Vercel blob storage.

---

## How to Run

Open `index.html` in a browser, or serve the folder with any static server (e.g. `npx serve .`). No build step required.
