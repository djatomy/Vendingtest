# Design System Document: Editorial Industrialism

## 1. Overview & Creative North Star: "The Industrial Curator"
This design system moves away from the sterile, "software-only" look of traditional B2B SaaS. Our North Star is **"The Industrial Curator."** It combines the unwavering reliability of heavy manufacturing with the sophisticated editorial precision required to engage Japanese executives. 

The layout strategy rejects the standard "bootstrap" grid. Instead, we utilize **Intentional Asymmetry** and **Tonal Depth**. Imagine a premium Japanese business journal: large serif headlines, generous white space, and high-quality photography layered with technical data overlays. We break the "template" look by allowing imagery of Vietnamese factory environments to bleed off-canvas or overlap with content cards, creating a sense of physical scale and forward momentum.

---

## 2. Colors: Tonal Architecture
We utilize a palette that feels grounded in reality. The Navy (#1A2C4E) provides the "Power," while the Off-white (#F8F6F0) provides "Reliability."

### The "No-Line" Rule
**Prohibit 1px solid borders for sectioning.** To define boundaries, use background color shifts only. A section using `surface-container-low` (#f5f3ed) sitting against the main `background` (#fbf9f3) creates a sophisticated transition that feels architectural rather than digital.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked physical materials.
- **Base Layer:** `background` (#fbf9f3)
- **Secondary Sectioning:** `surface-container` (#f0eee8)
- **Elevated Content/Cards:** `surface-container-lowest` (#ffffff)
Use this nesting to create importance. An infographic should sit on a `surface-container-highest` (#e4e2dd) to feel like a heavy, technical blueprint placed on a desk.

### Signature Textures & Glass
- **The Navy Gradient:** For CTAs and Hero backgrounds, do not use flat Navy. Use a subtle linear gradient from `primary` (#021738) to `primary_container` (#1a2c4e) at a 135-degree angle to simulate the sheen of precision-machined steel.
- **Industrial Glass:** For data overlays on factory imagery, use **Glassmorphism**. Apply `surface` at 70% opacity with a `20px` backdrop-blur. This ensures legibility while maintaining a visual connection to the "real work" environment in the background.

---

## 3. Typography: The Authority Scale
The interplay between **Noto Serif JP** (Authority) and **Be Vietnam Pro** (Modernity/Context) is critical.

*   **Display & Headlines (Noto Serif JP):** Used for core value propositions. The serif typeface communicates traditional Japanese business values: reliability and history. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create a "block" of powerful text.
*   **Body & UI (Be Vietnam Pro / Noto Sans JP):** Used for technical details and data. The switch to a clean Sans-Serif signifies the "modern efficiency" of the Vietnam-based operations.
*   **Labeling (Be Vietnam Pro):** All labels and data points should be in `label-md`, utilizing `on-surface-variant` (#44474e) to remain secondary to the narrative headlines.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often too "digital." We communicate depth through **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#f5f3ed) section. The contrast alone provides enough lift.
*   **Ambient Shadows:** If a floating element (like a mobile navigation bar) is required, use a shadow with a 32px blur and 4% opacity, using the `on-surface` color (#1b1c18) as the base. It should feel like a soft shadow cast by a paper on a desk, not a glow.
*   **The Ghost Border:** If accessibility requires a border, use `outline-variant` (#c5c6cf) at 20% opacity. **Never use 100% opaque borders.**

---

## 5. Components: Precision Engineered

### Data Tables (Industrial Spec)
*   **Styling:** Forbid internal grid lines. Use `surface-container-low` for the header row and `surface-container-lowest` for alternating body rows.
*   **Padding:** High vertical padding (1.5rem) to ensure data feels "premium" rather than "crowded."
*   **Accent:** Use a 4px vertical bar of `secondary` (Yellow #F5C400) on the far left of a "Highlighted Row" to denote key marketing insights.

### Info-graphics (The Blueprint Style)
*   **Visuals:** Use `outline` (#75777f) for thin, technical lines that mimic architectural drawings.
*   **Highlights:** Use `secondary_container` (#fdcc14) for bar charts or progress indicators to draw the eye instantly against the Navy/Off-white backdrop.

### Specialized Inquiry Form
*   **Inputs:** `surface-container-highest` background with a bottom-only "Ghost Border." Focus state shifts the bottom border to `secondary` (#745b00) 2px.
*   **The "Executive" Submit:** Large, full-width button using the Navy Gradient. Text should be `title-md` in `on-primary` (#ffffff) with 1.5rem letter-spacing for a sophisticated, cinematic feel.

### Buttons & Chips
*   **Primary Button:** Navy Gradient, `xl` (0.75rem) roundedness. No shadow.
*   **Secondary Button:** `surface-container-highest` background, `on-surface` text.
*   **Chips:** Use `surface-container-high` (#eae8e2) with `label-md` text. Perfect for tagging "Factory Location" or "Service Type."

---

## 6. Do’s and Don’ts

### Do:
*   **Do** overlap elements. Let a data table sit 40px over the edge of a factory photograph to create a layered, "collage" effect.
*   **Do** use the Spacing Scale religiously. Consistent white space is the difference between a "cheap" site and a "premium" experience.
*   **Do** use the Yellow accent sparingly. It is a surgical tool for conversion, not a primary decorative element.

### Don’t:
*   **Don't use dividers.** If you feel the need for a line, increase the vertical margin or change the `surface-container` tier of the next section.
*   **Don't use generic stock photos.** Imagery must feel "real"—raw concrete, steel beams, and focused workers in Vietnam. Avoid "smiling people in suits" at all costs.
*   **Don't use pure black.** Use `primary_fixed_variant` (#35466a) for high-contrast text to keep the palette sophisticated and integrated.