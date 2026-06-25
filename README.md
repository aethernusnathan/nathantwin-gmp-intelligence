# AI for GMP Documentation — A Practical Guide for Quality Managers

**Nathan Qin / NathanTwin Intelligence** · June 2026

An evidence-based guide to AI in pharmaceutical GMP documentation management.
Audience: QA directors, site quality heads, and quality managers at pharmaceutical companies
large and small who have tried AI tools and found them underdelivering.

The guide maps the **science of GMP documentation workflows**, assesses current AI tools honestly,
diagnoses the failure modes with regulatory citations, and describes the architecture that can
actually work — grounded in ICH Q10, FDA/EMA inspection data, and peer-reviewed evidence.

## What's Inside

- **GMP Manufacturing Process** — Documentation flow across API synthesis, drug product, QC, batch release
- **Supply Chain Oversight** — CMO/CDMO documentation obligations; traceability requirements
- **QMS Document Hierarchy** — L1 Policy through L6 APQR; the day-to-day review workflow
- **Live FDA Enforcement Feed** — Real-time GMP drug recalls via openFDA (loads on page open)
- **AI Tool Landscape** — Evidence-based capability matrix of Veeva, MasterControl, TrackWise, etc.
- **Failure Mode Analysis** — Scientific diagnosis of why AI fails in GMP environments
- **Compliant Architecture** — Four-layer design satisfying Annex 22 + 21 CFR Part 11
- **EMA Annex 22 Timeline** — Regulatory window 2026–2028 and what it means for tool selection

## Live APIs Wired

| Jurisdiction | Institution | API Status |
|---|---|---|
| 🇺🇸 US | FDA openFDA Drug Enforcement | ✦ Live REST API |
| 🇪🇺 EU | EMA / Europe PMC | ✦ Live REST API |
| 🇯🇵 Japan | PMDA | ◎ PubMed proxy |
| 🇨🇳 China | NMPA | ◈ Portal reference |

## Bruce Integration (Donna Research Agent)

Added GMP routing to Bruce (`bruce.py`) and five new API clients to `clinical_apis.py`:
- `openfda_drug_enforcement()` — FDA drug recalls / GMP enforcement
- `openfda_drug_event()` — FAERS adverse events
- `ema_medicines()` — EMA regulatory intelligence via Europe PMC
- `pmda_notices()` — Japan PMDA via PubMed affil filter
- `nmpa_china()` — China NMPA via PubMed affil filter

Ask Bruce: *"What GMP manufacturing recalls has FDA issued in the last 6 months?"* → live openFDA data.

## View

Open `index.html` in any browser. Live FDA enforcement data loads from openFDA on page load.

---

*Nathan Qin · NathanTwin Intelligence · Personal research project.*
