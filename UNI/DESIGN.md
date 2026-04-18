# Design System Documentation: Clinical Sanctuary

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Clinical Sanctuary."** 

To sell a premium hair growth product, we must bridge the gap between rigorous scientific efficacy and the organic, restorative nature of self-care. This system moves away from the "medical-industrial" look of traditional pharma and the "generic-minimalism" of D2C startups. Instead, it adopts a **High-End Editorial** approach. 

We break the "template" look by utilizing intentional asymmetry—where images might bleed off-canvas or overlap subtle background shifts—and a typography scale that treats words as visual anchors. The goal is to create a digital environment that feels breathable, expensive, and authoritative.

---

## 2. Colors
Our palette centers on the rejuvenating qualities of Mint and the sterility of Clinical White, balanced by sophisticated Grays.

### The "No-Line" Rule
Standard UI relies on 1px borders to separate content. **In this system, solid borders for sectioning are prohibited.** Boundaries must be defined solely through background color shifts. For example, a feature section in `surface-container-low` (#f2f4f3) should sit directly against the main `background` (#f8faf9) to create a soft, sophisticated transition.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers, like stacked sheets of fine, heavy-stock paper.
*   **Base:** `surface` (#f8faf9) for the overall page.
*   **Secondary Content:** `surface-container-low` (#f2f4f3) for subtle section breaks.
*   **Interactive Cards:** `surface-container-lowest` (#ffffff) to provide a "pop" of brightness against the background.
*   **Overlays/Modals:** `surface-container-highest` (#e1e3e2) for maximum contrast.

### The "Glass & Gradient" Rule
To elevate the "clinical" feel into "premium," use Glassmorphism for floating elements (like a "Verified Result" badge). Use `surface_container_lowest` with 70% opacity and a `20px` backdrop-blur. 
**Signature Textures:** For primary Call-to-Actions (CTAs) or high-impact hero backgrounds, use a subtle linear gradient transitioning from `primary` (#286954) to `primary-container` (#89cab0) at a 135-degree angle. This adds "soul" and depth that flat color cannot replicate.

---

## 3. Typography
We use **Manrope** across all scales. It is a modern, geometric sans-serif that feels engineered yet human.

*   **Display (lg/md):** Used for "Hero" headlines. These should be set with tight letter-spacing (-0.02em) to feel authoritative and editorial.
*   **Headline (lg/md):** Used for section titles. These act as the primary "hooks" for the user's eye.
*   **Title (lg/md):** Reserved for product names or benefit headers within cards.
*   **Body (lg/md):** Set in `on-surface-variant` (#3f4945) to reduce eye strain and maintain a soft, welcoming tone.
*   **Label (md/sm):** Always uppercase with increased letter-spacing (+0.05em) for "Clinical Data" points or small eyebrow headers.

The hierarchy is designed to convey "Expertise through Clarity." Large, confident display type suggests the brand has nothing to hide.

---

## 4. Elevation & Depth
Depth in this system is achieved through **Tonal Layering**, not structural scaffolding.

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#f2f4f3) section. The slight shift in luminosity creates a natural, soft lift.
*   **Ambient Shadows:** When a floating effect is required (e.g., a product bottle image), use extra-diffused shadows. 
    *   *Spec:* `0px 20px 40px rgba(25, 28, 28, 0.06)`. 
    *   Note the use of `on-surface` (#191c1c) at very low opacity to mimic natural light.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility in input fields, use the `outline-variant` (#bec9c3) at **20% opacity**. Never use 100% opaque borders.
*   **Glassmorphism:** Use semi-transparent layers for elements like "Floating Trust Badges" to let the mint and white tones bleed through, ensuring the UI feels integrated rather than cluttered.

---

## 5. Components

### Buttons
*   **Primary:** Background `primary` (#286954), Text `on-primary` (#ffffff). Shape: `lg` (0.5rem). Use the "Signature Gradient" on hover.
*   **Secondary:** Background `secondary-container` (#d0e4db), Text `on-secondary-container` (#54675f). No border.
*   **Tertiary:** No background. Text `primary` (#286954) with a `label-md` weight.

### Input Fields
*   **Style:** `surface-container-lowest` background with a "Ghost Border."
*   **States:** On focus, the ghost border becomes `primary` (#286954) at 100% opacity, and the label (using `label-md`) shifts to `primary`.

### Chips (Clinical Tags)
*   **Style:** Use `secondary-fixed` (#d3e7de) for the background and `on-secondary-fixed-variant` (#384b44) for text. Shape: `full` (pill). These should highlight ingredients like "Minoxidil" or "Biotin."

### Cards (The Benefit Block)
*   **Rule:** **Strictly no dividers.** Separate content using the `title-lg` for the header and `body-md` for the description. Use vertical white space (32px+) to separate the card from surrounding elements.

### Product Showcase (Custom Component)
*   An asymmetrical layout where the product image (with an Ambient Shadow) sits partially over a `primary-fixed` (#aef0d5) decorative background shape and partially over the `surface` background.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Negative Space:** Give every element room to breathe. If you think there's enough padding, add 16px more.
*   **Use Intentional Asymmetry:** Align text to the left but allow product imagery to be slightly offset to create a premium, editorial feel.
*   **Soft Transitions:** Use `surface-container` shifts to guide the user's eye down the landing page.

### Don't:
*   **No "Boxy" Layouts:** Avoid 12-column grids where every box is the same height. Use varied heights to create rhythm.
*   **Avoid Pure Black:** Never use #000000. Use `on-surface` (#191c1c) for all dark text to maintain the "Clinical Sanctuary" softness.
*   **No Standard Navbars:** This system focuses on the landing page experience. If navigation is needed, use a floating "Ghost" trigger or a simple text-link footer to avoid distracting from the product story.
*   **No Harsh Dividers:** 1px lines are the enemy of premium design. Let the color and space do the work.