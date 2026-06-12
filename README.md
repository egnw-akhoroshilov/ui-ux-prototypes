# AI Pricing Workstation — UI/UX Prototypes

Ten interactive high-fidelity prototypes of an **enterprise industrial computer-vision workstation** for a low-resolution production-floor touchscreen (**fixed canvas 1366 × 586, no scrolling**).

Operators photograph physical items, send them to AI analysis, review the suggested title / description / department / category / price, give thumbs-up / thumbs-down feedback, and then perform the final action: **Send to E-Comm · Print Tag · Salvage**.

## Run (no installation, no deployment)

Open `index.html` in any modern browser — or open any prototype file directly. Everything runs offline: React 18, Material UI v5, Babel standalone, Roboto and Material Icons fonts are vendored locally in `vendor/`.

## Prototypes

| # | File | Concept |
|---|------|---------|
| 1 | `prototype-1-conveyor-line.html` | Horizontal chevron step rail; camera bay left, work panel right |
| 2 | `prototype-2-split-console.html` | Dark left step-rail navigator; one large focused work area per step |
| 3 | `prototype-3-terminal-bay.html` | High-contrast dark HMI with indicator LEDs and mode tiles |
| 4 | `prototype-4-process-ledger.html` | Three columns (Capture / AI Review / Decision) unlocking left → right |
| 5 | `prototype-5-command-strip.html` | Giant step banner on top, fixed machine command bar at the bottom |
| 6 | `prototype-6-job-ticket.html` | Paper job-ticket with perforated stub and rubber-stamp APPROVED/REJECTED feedback |
| 7 | `prototype-7-gauge-deck.html` | Dark cockpit with circular four-segment step gauge and sweeping needle |
| 8 | `prototype-8-bellows.html` | Horizontal accordion — active stage expands, other stages collapse to vertical bars |
| 9 | `prototype-9-hazard-bench.html` | Safety-tape framed bench with blinking beacon step bar and labeled APPROVE/REJECT buttons |
| 10 | `prototype-10-andon-console.html` | Factory stack-light (andon) tower drives the workflow; shift queue strip at the bottom |

## Workflow states (all prototypes)

1. **Capture / Ready** — live camera preview, big CAPTURE button, ANALYZE locked until ≥1 photo.
2. **Analyzing** — camera preview off, full-screen touch lock prevents double submission.
3. **Review / Feedback Required** — operator must approve/reject **both** AI title and description.
4. **Ready for Action** — final action buttons unlock: Send to E-Comm / Print Tag / Salvage.

Each prototype is fully interactive end-to-end and also has a **DEMO — JUMP TO STATE** switcher below the canvas for instant preview of all four states.

## Design system

- Industrial neutral backgrounds (`#FCFCFC` / `#F8FAFC`, dark steel for HMI variants), text `#111111`, border `#0000001f`
- Industrial blue `#2196f3`, success green `#429a45`, warning/e-comm amber `#ed6c02`, error red `#b94646`
- Roboto / Arial; large type readable at arm's length; no purple gradients, no glassmorphism
- Minimum 56 px touch targets; no hover-only behavior; icons always paired with text; readable disabled states
- Status chips: Ready · Images Captured · Analyzing · AI Analysis Complete / Feedback Required · Ready for Action
