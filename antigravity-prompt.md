You are an expert front-end engineer. Your task is to build a high-performance, accessible, responsive static one-page website by reading three local assets in the current working directory:
1. `copy.md` (the single source of truth for all text content)
2. `design.jpg` (or `design.png` — the exact desktop and mobile UI reference)
3. `photo.jpg` (the real profile photo)

### 1. Architecture & Constraints
- Deliver only two clean files: `index.html` and `style.css`.
- Strictly vanilla HTML5 and CSS3: no JavaScript frameworks, no CSS frameworks, no build tools, no external script libraries, and no third-party CDNs (use modern system UI font stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif`).
- Semantic HTML markup (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- No contact form. Rely exclusively on verified public links provided in `copy.md`.

### 2. Copy & Metadata Precision
- Cross-reference `copy.md` for all headings and text blocks. Do not invent any copy, claims, or lorem ipsum.
- Page `<title>`: `Mahfoudh Arous — Software Engineer, React Specialist & Mentor`
- Meta Description: `Software Engineer, React & JavaScript specialist, and Mentor. Building SaaS, web applications, and interactive learning tools.`
- Sections:
  - Hero: "Hi, I'm Mahfoudh Arous" with the exact sub-headline and a CTA button "View my work" anchoring to `#projects`.
  - About Me: Exact text from `copy.md` covering freelance, Sonelgaz/Siemens experience, and trilingual capability (Arabic, French, English).
  - Skills & Expertise: Render pill tags based on `copy.md` and the visual reference (React, JavaScript, WordPress, Public Speaking, Technical Translation, Node.js, Git).
  - Experience: The 4 distinct roles from `copy.md` (Mentor at OpenClassrooms, Full-stack Developer on Fiverr, Software Engineer at Sonelgaz/Siemens, Software Engineer at CNEP-Banque).
  - Featured Work: Cards for "Interactive React Code Lab", "DevLingo", and "Freelance Projects".
  - Let's Connect: "Building a web product or learning tool? Let's connect." with the direct LinkedIn link (`https://www.linkedin.com/in/mahfoudh-arous/`).

### 3. Visual Styling & Color Tokens (Sampled from `design.jpg`)
Apply these exact hex values:
- Dark Hero / Header Background: `#0B132B` (deep navy)
- Light Page Background (Main Content): `#F4F6F9` or `#FFFFFF` for the central content container
- Dark Section / Card Background: `#1C2541` (dark slate blue)
- Dark Card Inner / Sub-surfaces: `#243056`
- Primary Brand Blue (Buttons & Badges): `#1D68F2` / `#2563EB`
- Vibrant Cyan Accent (Glow, Highlights, Tech Badges): `#00D2D3` / `#06B6D4`
- Text Colors:
  - White / Off-white (dark surfaces): `#FFFFFF` and `#94A3B8` (muted text)
  - Dark Charcoal (light surfaces): `#0F172A` and `#475569` (body text)
  - Card Headings: `#FFFFFF`

### 4. Component Details & Profile Photo
- **Profile Image (`photo.jpg`)**:
  - Replace the placeholder avatar in the hero with `<img src="photo.jpg" alt="Mahfoudh Arous">`.
  - Enforce a crisp circular crop (`border-radius: 50%; object-fit: cover;`).
  - Add the luminous cyan border/glow effect matching `design.jpg` (`box-shadow: 0 0 24px rgba(6, 182, 212, 0.45); border: 3px solid #06B6D4;`).
  - Set explicit `width` and `height` attributes to prevent Cumulative Layout Shift (CLS).
- **Cards & Layout**:
  - Rounded corners (`border-radius: 12px` to `16px`).
  - Experience section: clean timeline/bulleted list with glowing indicator dots.
  - Featured Work: multi-column grid on desktop, single-column stacked on mobile.

### 5. Responsiveness & Mobile Menu
- Fluid responsiveness starting at `360px` width up to large desktop screens.
- **Desktop**: Horizontal navigation links (`About`, `Skills`, `Experience`, `Projects`, `Contact`) aligned right, hero layout with side-by-side avatar and intro text, 2-column About/Skills grid, 2-column Experience grid, 3-card Projects row.
- **Mobile (< 768px)**:
  - Single-column flow with centered hero elements.
  - Accessible mobile menu using a pure CSS or lightweight vanilla toggle pattern (`aria-expanded`, clean drawer or collapsible dropdown).
  - Touch-friendly tap targets (minimum 44x44px).

### 6. Accessibility (a11y)
- WCAG AA contrast compliance across all text against dark and light backgrounds.
- High-visibility keyboard focus indicators (`:focus-visible { outline: 2px solid #00D2D3; outline-offset: 3px; }`).
- Semantic landmarks and valid ARIA attributes where applicable.

### 7. Completion Deliverable
1. Write and save `index.html` and `style.css`.
2. Open a local live preview to confirm visual match with `design.jpg`.
3. Provide a concise checklist of verified items:
   - File creation and asset path verification (`photo.jpg`)
   - Visual parity check against `design.jpg` (desktop & mobile)
   - Copy accuracy check against `copy.md`
   - Responsive layout down to 360px
   - Accessibility check (focus states, alt text, color contrast)