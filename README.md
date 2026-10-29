# Meridian Workforce Decision Lab

A standalone, interactive **workforce transition decision-support prototype** for the fictional Project Meridian case study. The product demonstrates a **demand-led redeployment** approach: understand exposure, validate receiving-work demand, review capability evidence, and make conditional workforce transition decisions.

> **Case-study demonstration, not a production HR system or a forecast of actual employees.** Regional, workforce-family and economic scenario inputs are synthetic unless expressly identified as case-brief inputs.

## Run locally

There is **no installation or build step**. Open `index.html` in a modern desktop browser (Chrome, Edge, Firefox, or Safari). The app's HTML, CSS and JavaScript are all contained in this file. No CDN, account, or API is required.

Alternatively, serve the repository locally:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Publish with GitHub Pages

1. Create a GitHub repository and upload **the contents** of this package to its root (especially `index.html`).
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`, then save.
5. Once GitHub Pages finishes deploying, open the URL shown in Pages settings. Usually it follows `https://<account>.github.io/<repository>/`, but use GitHub's actual URL.
6. Test the page in a private/incognito browser window to verify it is available without logging in, and put the **verified URL** into the final submission PDF.

Other static hosts (Netlify, Cloudflare Pages, etc.) can serve `index.html` without configuration.

## Product walkthrough

1. **Enterprise exposure:** Compare 12 job-family illustration rows, including absolute exposed work equivalents, time-to-impact and evidence confidence. Field Metering is prioritized because its *urgency and evidence* are stronger—not because it must have the largest absolute exposure.
2. **Scenario Lab (AHA):** Compare **900 assumed receiving-work equivalents** with approximately **5,146 required at month 18**. Set *Contractor substitution demand* to **Zero contractor**, and toggle *Rollout sequencing authority* between **Cannot gate** and **Can gate**. The displayed synthetic curve, unresolved gap and guidance update.
3. **Demand / capabilities:** Explore how verified destination-work requirements and voluntarily provided task evidence inform human-reviewed matching.
4. **Board decisions:** Review conditions, governance constraints, residual capacity and the least-confident decision.

## Key analytical distinctions

- **Strategy:** demand-led redeployment; **selective gating** is only a conditional operational lever.
- **70%** is task/workload automation *exposure* in the case; actual displacement depends on realization over time.
- A **work equivalent is not a person to dismiss**. The unresolved gap is simulated capacity pressure, not a list of redundant staff.
- Assumed receiving-work capacity is **not confirmed vacancies**.
- Gating can shift *when* pressure materializes; it does not create receiving work or erase the structural gap.
- Cash ROI is highly conditional. **Contractor substitution is not evidenced in the brief**; the model's +290% and −100% outcomes are bounding scenarios when contractor savings are the only modeled cash benefit category. Other categories need Finance validation.
- Scenario curves are **model-anchored interpolations**, not a full recalculation of the spreadsheet's 36 monthly formulas.
- No automated employment decisions, layoffs, suitability ranking, or real employee data are included.

See [docs/MODEL_NOTES.md](docs/MODEL_NOTES.md) for assumptions and known limits.

## Repository structure

```text
.
├── index.html             # Entire standalone app (HTML + CSS + JS)
├── README.md              # Setup, publishing, demo instructions
├── .nojekyll              # Serve static content as-is on GitHub Pages
└── docs/
    └── MODEL_NOTES.md     # Assumptions, data provenance, limitations
```

## Current status

**Prototype v2 for review**; not independently validated against live Client data. Source-script syntax was checked during development, but this package does not claim cross-browser end-to-end QA or public hosting. Review visual behavior, toggle states, and model claims before submission.
