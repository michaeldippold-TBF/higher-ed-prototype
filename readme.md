# README

## Project Goal

This project delivers a **prototype microsite** for a Higher Education client who has requested a subscription form for tiered access. The purpose of this prototype is to give the client something **interactive and tangible** to review before full implementation, helping secure client approval and understanding.

### Original Prompt

> Background:
>
> A Higher Education client has requested a subscription form for tiered access. They need a working prototype to help understand what we are proposing be implemented more clearly before work starts. The goal here is client approval and understanding.
>
> Functional Requirements:
>
> * User Registration Form
> * Offers 3 levels of subscription
> * Prototype only to verify you’re on the right path for client request
>
> Technical Requirements:
>
> * Prototype is usable/reviewable - not just static
> * Showcase as microsite
> * Exportable to Figma for refinement by design team

---

## Prototype Overview

The prototype is a **single-page microsite** (`index.html`) that:

1. **Presents three tiered subscription options** (Student, Faculty, Research) with feature breakdowns.
2. **Includes a registration form** with fields for name, email, institution, role, and password.
3. **Validates input** to ensure required fields are completed before submission.
4. **Stores form submissions locally (LocalStorage)** to mimic persistence.
5. **Provides an Admin Preview tab** where the stored registrations can be viewed in a table, filtered via search, seeded with sample data, or cleared entirely.
6. **Offers export tools**:

   * **CSV download** of stored registrations.
   * **Design Tokens (JSON)** export for use in Figma tokens plugins.
   * **SVG Frame Export** that recreates the page’s layout for direct Figma import.

---

## Design Decisions

### Tiered Subscription Cards

* Three tiers are laid out as **responsive cards** with price, badge, and feature list.
* Color palette uses the client’s defined scheme (`#1d1d1d`, `#e5e5e5`, `#d3d3d3`, `#9c0b12`, `#8d0d13`).
* Selection is interactive: clicking a card updates the registration form’s “Selected tier” label.

### Registration Form

* Standard fields (first/last name, email, institution, role, password).
* Additional checkboxes for newsletter opt-in and Terms of Service.
* Uses built-in HTML5 validation with custom feedback logic to enable/disable the **Complete Registration** button.

### Admin Preview

* Provides transparency into what data is being collected.
* Simulates admin-side viewing of registrations.
* Search field supports quick filtering.
* Includes buttons to **seed sample data** (for demo purposes) and **clear stored data**.

### Export Features

* **CSV Export** helps illustrate practical reporting needs.
* **Tokens JSON** captures design tokens (colors, fonts, radii, shadows) for designer handoff.
* **SVG Export** produces a clean frame of the microsite UI for drag-and-drop into Figma, letting designers refine the layout.

### Technical Choices

* **Self-contained file**: HTML, CSS, and JS bundled in one file for portability.
* **No dependencies**: No frameworks or libraries to avoid overhead.
* **LocalStorage persistence**: Lightweight simulation of backend behavior.
* **Accessibility**: Aria roles, focus states, and keyboard interaction for tier selection.

---

## How to Use

1. Unzip the package.
2. Open `index.html` in any modern browser.
3. Use the **Subscribe** tab to:

   * Select a subscription tier.
   * Complete and submit the form.
4. Switch to **Admin Preview** to:

   * View stored submissions.
   * Search, seed, or clear records.
   * Export CSV.
5. Use the **toolbar buttons** (top right) to export SVG for Figma or tokens JSON.

---

## Conclusion

This prototype meets the client’s stated requirements:

* Demonstrates **tiered subscription access** visually and interactively.
* Provides a **registration workflow** that feels real.
* Simulates **admin reporting features**.
* Supports **handoff to design tools (Figma)** for refinement.

It is a proof-of-concept — not a production-ready app — but sufficient for client approval and next-phase design discussions.
