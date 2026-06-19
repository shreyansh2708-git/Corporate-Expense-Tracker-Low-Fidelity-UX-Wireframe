# Corporate Expense Tracker — Low-Fidelity UX Wireframe

A grayscale, low-fidelity wireframe exploring the end-to-end user flow for corporate expense logging — from receipt capture to HR approval tracking.

🔗 **Live Prototype:** (https://www.figma.com/design/h1GtRvWEsOr40zUvf3E7rx/Corporate-Expense-Reimbursement-Tracker--Mobile-App-?node-id=0-1&t=fe3CHnwovseUEq3f-1)

<img width="3948" height="2915" alt="Full Wireframe — All 3 Screens Side-by-Side" src="https://github.com/user-attachments/assets/81291cae-9e50-487a-83e2-4a0b304ff9d6" />

---

## Why This Project

Expense reporting is one of those everyday corporate workflows that's quietly broken almost everywhere — employees lose receipts, fill the same data in twice, and have no visibility into where their reimbursement actually stands once it's submitted. I wanted to design a flow that removes manual data entry as much as possible and gives the user constant status feedback, without touching any visual branding yet — just structure, hierarchy, and flow.

So I deliberately stayed in **grayscale, low-fidelity wireframe mode** for this entire case study. No color, no gradients, no polish. The goal was to stress-test the *information architecture and interaction logic* before a single design decision gets influenced by a color palette or brand kit.

## Process

I broke the flow into three core moments a user goes through when filing an expense:

1. **Capture** — getting the receipt into the system with minimal friction
2. **Verify** — confirming what the system extracted is correct, without re-typing everything
3. **Track** — knowing where the claim stands after submission

Each screen below maps to one of those moments.

---

## Screen 1 — Receipt Scanner

<img width="307" height="326" alt="Screen 1 — Receipt Scanner" src="https://github.com/user-attachments/assets/573e9478-bbd8-4894-bf6b-4841aa36c42a" />

Full-bleed camera interface as the entry point — no menu, no extra taps before the user can start capturing. I used dashed L-shaped corner brackets to define the scan zone, since this is a pattern most users already recognize from payment apps and document scanners — it borrows familiarity instead of teaching a new gesture.

- Shutter button anchored bottom-center, oversized for thumb reach
- Flash and gallery controls flank it symmetrically so the eye doesn't have to search
- Helper text below the scan zone ("Align receipt within the frame for auto-extraction") sets expectations for *why* the frame exists, not just *what* to do

**Design decision:** I used a boxed `×` as the placeholder convention for the camera feed and receipt thumbnail instead of a photorealistic mockup — this keeps the wireframe honest about being a structural blueprint, not a finished visual.

## Screen 2 — Expense Form (AI Auto-Fill)

<img width="309" height="310" alt="Screen 2 — Expense Form" src="https://github.com/user-attachments/assets/a4dc53aa-1cd3-4215-8fcc-e678c38253ac" />

This is the screen I spent the most time on, because it's where trust in the system is either built or broken. If a user has to double check every field manually, the "AI extraction" feature is pointless from a UX standpoint.

- A receipt thumbnail stays visible at the top so the user has a reference point while reviewing extracted data — they shouldn't have to scroll back or re-scan to verify
- I added an explicit `AI OCR COMPLETE` badge near the header — a small thing, but it's a deliberate trust signal. It tells the user *the system did the work*, not just that fields happen to be filled in
- Pre-filled fields are visually distinguished from empty fields the user still needs to touch (`auto-fill ✓` marker) — this avoids the common pattern-recognition failure where users skim a form and miss the one field that didn't get extracted correctly
- Primary CTA ("Submit for HR Approval") is solid and high-contrast; the secondary action ("Retake Photo") is outlined — standard visual weight hierarchy so the user's eye lands on the intended next step first

## Screen 3 — Status Tracker

<img width="316" height="327" alt="Screen 3 — Status Tracker" src="https://github.com/user-attachments/assets/decaaada-6ce6-48eb-acda-b1f9f8df7c63" />

The most overlooked screen in most expense tools is the one after submission — and it's usually the one users check most often, out of anxiety more than anything else.

- Segmented control (All / Pending / Approved) lets users filter without leaving the screen
- Status pills use **fill vs. outline** as the differentiator rather than relying on color, which was the whole point of doing this in grayscale — proving the hierarchy reads clearly even without a color system to lean on. Filled = Approved (resolved, settled), Outlined = Pending (still in motion)
- Each card surfaces merchant, amount, category, and date upfront — the four data points a user actually scans for, with nothing extra competing for attention

---

## Design Constraints (Intentional)

- **Strictly grayscale** — black, white, and grays only. No color was used anywhere in this study.
- **Geometric placeholders** — boxes, circles, and `×` markers instead of real imagery, to keep focus on layout and flow rather than content polish
- **Annotated externally** — leader lines and labels sit outside the device frames so the reasoning behind each decision is visible alongside the screen itself, not buried in a separate doc

## What I'd Test Next

- Whether users actually trust the "auto-fill ✓" indicator enough to skip manual verification, or whether it needs a confidence score
- Whether the Pending/Approved fill-vs-outline distinction holds up for color-blind users without the fill needing to be paired with a label (it currently is, as a safety net)
- A rejected/flagged state for the status tracker — the current flow only accounts for Pending and Approved, not disputes

## Tools

Figma · Wireframing · Information Architecture · Interaction Design · Grayscale UI Systems

---

*Part of a series of UI/UX case studies exploring product flows before visual design.*
