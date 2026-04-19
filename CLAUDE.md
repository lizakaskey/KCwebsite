# Kaskey Consulting — Website Build Instructions

## Always Do First
- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.
- **Check for brand assets** before designing. Use real assets where available — do not use placeholders where real logos, colors, or images exist.

---

## What We're Building

A custom marketing website for **Kaskey Consulting**, a fractional Chief of Staff service for high-net-worth, time-starved families. The founder is Liza Kaskey, who comes from an investment banking background. This is not a household help service — it is operational partnership at the family level.

The website replaces an existing Squarespace site at **kaskeyconsulting.co**. When complete, the single HTML file will be deployed to Netlify via drag and drop — no build steps, no dependencies, no local server required.

---

## The Brand

**Who this is for:** Dual-income, high-achieving families with kids. They are not failing — they are just always slightly reactive. They have the resources to live well. What they're missing is someone holding the picture and running it forward.

**What Kaskey Consulting does:** Manages the life admin that busy families never have time to be proactive about. Dentist appointments, travel, vendor relationships, gift obligations, summer camp research, recurring household commitments. Built on simple, collaborative systems designed around how the family already operates. Ongoing retainer model — not a one-time project.

**The core differentiator:** A personal assistant waits for your instructions. Kaskey Consulting makes sure you never have to give them.

**Voice:** Warm but elevated. Confident. Tight. Never over-explaining. Never framing the client's life as broken or chaotic. No exclamation marks. Shorter is almost always better.

**Visual aesthetic:** Refined, editorial, luxury-minimal. High-end editorial meets approachable warmth. Not cold or corporate. Not busy or cluttered. Typography should feel considered and distinctive — like it belongs in a high-end shelter or lifestyle magazine.

---

## Site Structure

**Single page, scroll-based.** Sections in order:

1. **Hero** — Lead with the feeling, not the service. The hook is emotional, not descriptive.
2. **The Problem** — Name the mental load without making clients feel judged. Relatable and specific.
3. **What I Do** — The five buckets: Calendar & Time, Relationships & Obligations, Household & Vendors, Travel & Logistics, Research & Decision Support.
4. **How It Works** — Onboarding, collaborative system design, ongoing retainer, standing check-in.
5. **Why This Is Different** — Chief of Staff vs. PA vs. House Manager. Clear, clean, confident.
6. **About Liza** — Investment banking background, systems thinker, works with a small number of families by design.
7. **Contact / Inquiry** — Simple. Name, email, brief description of their household. No lengthy forms.

---

## Core Copy (Use and Adapt)

**Positioning statement:**
"I am a fractional Chief of Staff for busy families. I manage the life admin that educated, high-achieving people never have time to be proactive about — and I stay involved on an ongoing basis so nothing falls through the cracks."

**The problem:**
"Most families I work with are managing demanding careers, kids, properties, and a full social life. They're not failing. They're just always slightly behind on the proactive stuff. The dentist appointments that don't get made until someone gets a toothache. The anniversary dinner that gets planned the week of. The summer camp research that happens in April when everything is already full. They have the resources to live well — what they're missing is someone holding the picture and running it forward."

**The differentiator:**
"A personal assistant waits for your instructions. I make sure you never have to give them."
"A house manager runs your home. A personal assistant runs your inbox. I run your life — proactively, and in partnership with you."

**The retainer value:**
"I work with a small number of families at a time, by design. The model only works if I know your life well enough to anticipate it. That takes time and it takes trust — and I take both seriously."

**The background:**
"I come to this work with a background in investment banking — which means I think in systems, I operate with rigor, and I understand what it means to support high-stakes decision making for demanding principals."

---

## Color Palette — Use These Exact Values Only

Define all colors as CSS variables at the top of every file. Never use default Tailwind colors (indigo, blue, etc.).

```css
:root {
  --cream:    #F5F1EB; /* Primary background */
  --linen:    #EAE3D6; /* Secondary background */
  --charcoal: #2B2B2B; /* Primary text */
  --espresso: #452F1E; /* Deep accent, strong moments */
  --chestnut: #8B5E3C; /* Mid accent */
  --forest:   #3C4A40; /* Secondary accent */
  --gold:     #C0A97A; /* Highlight, warm detail */
  --taupe:    #9C8E7B; /* Supporting neutral, captions */
}
```

---

## Typography Rules

- **Never** use Inter, Roboto, Arial, or system fonts
- **Always** pair a distinctive display/serif font with a clean, refined sans-serif body font
- Large headings: tight tracking (`letter-spacing: -0.03em`), strong weight
- Body text: generous line-height (`1.7`), comfortable reading size
- Captions and labels: taupe (`#9C8E7B`), slightly smaller, spaced
- Type should feel like it belongs in a high-end lifestyle or shelter magazine

---

## Design Guardrails

**Shadows:** Never flat `box-shadow`. Use layered, color-tinted shadows with low opacity.

**Gradients:** Layer multiple radial gradients. Add grain/texture via SVG noise filter for depth where appropriate.

**Animations:** Only animate `transform` and `opacity`. Never `transition-all`. Use smooth, spring-style easing. Gentle fade-ins on scroll — nothing that feels like a template.

**Interactive states:** Every clickable element needs hover, focus-visible, and active states. No exceptions.

**Spacing:** Use intentional, consistent spacing tokens. Not random steps.

**Depth:** Surfaces should have a layering system — base, elevated, floating. Not everything at the same z-plane.

**Images:** If used, add a gradient overlay and color treatment. Never raw stock photos.

**Negative space:** The site should breathe. Density is the enemy.

---

## Build Rules

- Single `index.html` file — all styles and scripts inline
- Tailwind CSS via CDN if used: `<script src="https://cdn.tailwindcss.com"></script>`
- All brand colors defined as CSS variables — never hardcoded inline
- Placeholder images via `https://placehold.co/WIDTHxHEIGHT` only where real assets don't exist
- Mobile-first responsive — most traffic will arrive from TikTok on phones
- Design for Netlify drag-and-drop deployment — zero build steps, zero dependencies
- One clear CTA throughout: "Work with me" or "Inquire" — consistent, never pushy
- When in doubt, do less. Restraint is the aesthetic.

---

## Hard Rules

- Do not use `transition-all`
- Do not use default Tailwind blue or indigo as any color
- Do not add sections or content not specified in the site structure
- Do not use generic AI aesthetics — no purple gradients, no tech startup vibes
- Do not make the client feel like their life is broken or chaotic — language is always opportunity-oriented
- Do not over-explain the service — shorter copy almost always wins

---

## What Claude Should Always Remember

- Liza's voice is warm, confident, and never over-explains
- The client is a peer, not a customer to be sold to
- This is not household help — every word should reflect operational partnership
- The systems piece matters — built collaboratively, fits how the family actually lives
- Every design decision should ask: would a discerning, time-starved New York family trust this instantly?
