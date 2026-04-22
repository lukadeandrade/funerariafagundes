```markdown
# Design System Document: The Quiet Sanctuary

## 1. Overview & Creative North Star
The design system for Funerária Fagundes is guided by the Creative North Star: **"The Quiet Sanctuary."** 

In the funeral industry, digital interfaces often feel either clinical or overly somber. This system breaks that mold by adopting a **High-End Editorial** approach. We move away from standard "grid-and-box" layouts in favor of intentional asymmetry, generous whitespace, and tonal layering. The goal is to provide a digital environment that feels like a physical sanctuary—hushed, premium, and deeply respectful. 

By utilizing overlapping elements and a dramatic typographic scale, we create a sense of "Architectural Peace," where the interface doesn't just provide information, but offers a moment of repose for the user.

---

## 2. Colors & Atmospheric Depth
Our palette is rooted in the depth of the night and the serenity of nature. We use color not just for branding, but to define space and emotion.

### The "No-Line" Rule
To maintain a high-end, seamless feel, **1px solid borders are prohibited for sectioning.** Boundaries must be defined through:
*   **Background Shifts:** Transitioning from `surface` (#f9f9f9) to `surface_container_low` (#f3f3f3).
*   **Tonal Transitions:** Using subtle shifts between neutral tiers to imply structure without creating visual "noise."

### Surface Hierarchy & Nesting
Think of the UI as layers of fine paper. 
*   **Level 0 (Base):** `background` (#f9f9f9).
*   **Level 1 (Content Sections):** `surface_container` (#eeeeee).
*   **Level 2 (Cards/Interactive):** `surface_container_lowest` (#ffffff) to provide a soft "lift."

### Glass & Gradients
For floating elements (like navigation bars or modal overlays), use **Glassmorphism**. Apply `surface` with 80% opacity and a `20px backdrop-blur`. 
**Signature Texture:** Use a linear gradient from `primary` (#03192e) to `primary_container` (#1a2e44) at a 135-degree angle for hero sections. This adds a "velvet" depth that flat color cannot replicate.

---

## 3. Typography: The Editorial Voice
We pair the timeless elegance of **Playfair Display** (Serif) with the modern precision of **Inter** (Sans).

*   **Display & Headlines (Playfair Display):** These are our "Statement" pieces. Use `display-lg` (3.5rem) with slightly tighter letter-spacing (-2%) to create an authoritative yet poetic header.
*   **Body & Labels (Inter):** Designed for maximum legibility. For `body-lg`, use a line-height of 1.6 to ensure that users under emotional stress can digest information easily.
*   **The Contrast Principle:** Always pair a large Serif headline with a clean, wide-margined Sans-Serif body. This contrast signals "Curated Excellence."

---

## 4. Elevation & Depth
We eschew traditional drop shadows for **Ambient Light** and **Tonal Layering.**

*   **The Layering Principle:** Depth is achieved by stacking. Place a `surface_container_lowest` card on top of a `surface_container_high` background. The slight difference in hex value creates a "natural" lift.
*   **Ambient Shadows:** If a floating effect is required (e.g., a primary CTA button), use a shadow with a 24px blur, 4% opacity, using the `primary` color as the shadow tint. It should look like a soft glow, not a dark stain.
*   **The Ghost Border Fallback:** If a border is required for accessibility, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.

---

## 5. Components & Primitive Styling

### Buttons (The "Soft-Touch" Interaction)
*   **Primary:** Background `primary` (#03192e), Text `on_primary` (#ffffff). Corner radius: `md` (0.375rem). Use a subtle hover shift to `primary_container`.
*   **Secondary (Serenity Action):** Background `secondary` (#50652a), Text `on_secondary`. Used specifically for "Support" or "Contact" actions to evoke a sense of calm.
*   **Tertiary:** No background. Underlined with a `2px` stroke of `primary_fixed_dim` sitting 4px below the text baseline.

### Cards & Information Modules
*   **Strict Rule:** No divider lines. Separate content using `spacing-xl` (vertical whitespace) or by nesting a `surface_container_highest` header inside a `surface_container` card.
*   **Imagery:** All images must have a subtle `0.25rem` (sm) corner radius to match the "softened" brand identity.

### Input Fields
*   **Styling:** Use "Soft Inset" styling. Background `surface_container_low`, no border, only a 2px bottom stroke in `outline_variant` that transforms to `primary` on focus.

### Specialized Components
*   **The Tribute Timeline:** A vertical list using `secondary` (Olive) dots to mark milestones, connected by a 1px `outline_variant` dashed line (the only exception to the line rule).
*   **The Support Float:** A glassmorphism-based persistent action button for "Immediate Assistance," using `surface_bright` with a blur effect.

---

## 6. Do's and Don'ts

### Do:
*   **Use Asymmetry:** Place a headline on the left and the body text slightly offset to the right to create a premium, "magazine" feel.
*   **Embrace the "Olive":** Use the `secondary` (#556b2f) sparingly as a "Life & Peace" accent—specifically for icons related to flowers, legacy, or support.
*   **Prioritize Breathing Room:** If a layout feels "busy," double the margin. Space is the ultimate luxury.

### Don't:
*   **Avoid Pure Black:** Never use #000000. Use `primary` or `tertiary` for deep tones to keep the interface feeling "organic" rather than "digital."
*   **No Sharp Corners:** Avoid the `none` (0px) roundedness. Everything should feel slightly softened to the touch.
*   **No Aggressive Animations:** Use slow, "ease-in-out" transitions (300ms+). Avoid "snappy" or "bouncy" movements; the interface should move with the grace of a slow tide.

---

**Director's Final Note:** 
This system is not a template; it is an atmosphere. Every pixel should contribute to a feeling of being "held" and "respected." When in doubt, add more whitespace and remove a line. Let the typography and the deep navy tones do the heavy lifting.```