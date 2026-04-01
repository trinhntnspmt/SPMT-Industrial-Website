# Design System Specification: Industrial Sophistication

## 1. Overview & Creative North Star: "The Architectural Blueprint"
This design system is engineered for **Công ty SPMT** to bridge the gap between heavy industrial reliability and high-end corporate precision. Our Creative North Star is **"The Architectural Blueprint."** 

Unlike standard "out-of-the-box" industrial sites that rely on clunky grids and heavy borders, this system utilizes intentional asymmetry, expansive white space, and tonal layering. We move away from "template" aesthetics by treating the UI as a series of precision-machined layers. The goal is a digital experience that feels as solid as a steel beam but as refined as a luxury timepiece. We convey Ngọc Trinh’s vision through an editorial lens: bold, authoritative typography paired with "breathable" layouts that suggest efficiency and modern scale.

---

## 2. Colors: Tonal Precision
We move beyond flat "Corporate Blue." By utilizing a range of blues and neutral surfaces, we create a sense of mechanical depth.

*   **Primary Palette (The Core):** 
    *   `primary` (#004085) serves as our "Anchor Blue." It represents the heavy-duty reliability of SPMT.
    *   `primary_container` (#1d57a7) is used for active states and secondary emphasizes, providing a softer, luminous blue that adds "soul" to the interface.
*   **The "No-Line" Rule:** To achieve a premium look, **1px solid borders are strictly prohibited** for sectioning. Boundaries must be defined by:
    *   **Background Shifts:** Transitioning from `surface` (#f7fafd) to `surface_container_low` (#f1f4f7).
    *   **Tonal Nesting:** A `surface_container_lowest` (#ffffff) card sitting on a `surface_container` (#ebeef1) background.
*   **The Glass & Gradient Rule:** 
    *   For Hero sections or major CTAs, use a subtle linear gradient: `primary` to `primary_container` at 135 degrees. 
    *   Floating navigation or overlays must use **Glassmorphism**: `surface` at 80% opacity with a `24px` backdrop-blur to create a "frosted glass" effect.

---

## 3. Typography: The Editorial Engine
The typography pairing reflects industrial strength (`Manrope`) and functional clarity (`Inter`).

*   **Display & Headlines (Manrope):** Use `display-lg` (3.5rem) and `headline-lg` (2rem) for high-impact messaging. These should be **Bold (Weight 700)** to mirror the "Industrial" requirement. They provide the "Editorial" weight that makes the system feel expensive.
*   **Body & Labels (Inter):** All functional text uses `body-md` (0.875rem). Inter’s geometric neutrality ensures that technical data remains legible and trustworthy.
*   **Visual Hierarchy:** Large typographic scales (e.g., `display-md` next to `label-md`) create the intentional asymmetry required to break the "standard" UI look.

---

## 4. Elevation & Depth: Tonal Layering
We reject the 2010-era "drop shadow." Depth is achieved through the **Layering Principle.**

*   **The Stacking Order:** 
    1.  Base: `surface_container_low`
    2.  Section: `surface`
    3.  Card/Element: `surface_container_lowest`
*   **Ambient Shadows:** Use shadows only for interactive elements that "lift" (like a button on hover). Use a large blur (`32px`) and very low opacity (`4%`) using a tint of `on_surface` (#181c1e).
*   **The "Ghost Border" Fallback:** If a divider is functionally required, use the `outline_variant` (#c2c6d4) at **15% opacity**. It should be felt, not seen.
*   **Industrial Corners:** Use `sm` (0.125rem) for technical components (inputs, data cells) and `lg` (0.5rem) for containers to balance "Industrial" rigidity with "Modern" softness.

---

## 5. Components: Engineered Efficiency

### Buttons (The "Actuators")
*   **Primary:** Solid `primary` background with `on_primary` text. Use `md` (0.375rem) roundedness. No shadow at rest; a subtle `primary_container` glow on hover.
*   **Secondary:** `surface_container_highest` background. This creates a "machined metal" look without the harshness of a border.

### Input Fields (The "Specifications")
*   **Design:** Use `surface_container_low` as the fill. Replace the bottom border with a 2px stroke of `primary` only when **Focused**. At rest, the input should have no visible border, merging into the surface.

### Cards & Data Lists
*   **Prohibition:** Never use divider lines.
*   **Separation:** Use `spacing-8` (1.75rem) to separate content blocks. For data lists, use alternating backgrounds (`surface` and `surface_container_low`) to define rows.

### Signature Component: The "Industrial Progress Rail"
A custom progress tracker for logistics/projects using `tertiary` (#722b00) as the accent. This high-contrast "Rust/Safety Orange" color should be used sparingly for status alerts or critical path milestones, providing a professional industrial nod.

---

## 6. Do's and Don'ts

### Do:
*   **Use Wide Margins:** Use `spacing-24` (5.5rem) for outer page gutters to give the industrial content "room to breathe."
*   **Embrace Negative Space:** Allow headlines to sit alone in large `surface` areas.
*   **Layering over Outlining:** Always ask "Can I define this area with a background color shift instead of a line?"

### Don't:
*   **No Pure Black:** Never use #000000. Use `on_surface` (#181c1e) for all "black" text to maintain tonal softness.
*   **No Standard Shadows:** Avoid CSS `box-shadow: 0 2px 4px rgba(0,0,0,0.5)`. It looks cheap. Use our Ambient Shadow rules.
*   **No Crowding:** Industrial design is about scale. Avoid cramming multiple cards into a single row; use fewer, larger containers.

---
**Director's Final Note:** This system is not just a UI; it is a manifestation of SPMT’s reliability. Every pixel must feel intentional, every margin must feel calculated, and every color shift must feel like a precision-engineered transition.