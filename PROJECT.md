# SFC Cutter Performance Tracker

## What This Is

A web-based yield tracking system for a seafood and meat processing company. Supervisors enter batch data after each cutting run — capturing source weight, output weights (primary yield, usable trim, by-product), cutter identity, species, and timing. The system calculates yield percentages and lbs/hour automatically, then surfaces this data in a dashboard where the director can view cutter performance summaries and detailed batch records.

## Core Value

Measure and track cutter performance through accurate yield and throughput data so the director can identify efficiency opportunities across the cutting floor.

## Requirements

### Validated

(None yet — ship to validate)

### Active

- [ ] Supervisor can enter batch data (cutter, species, source weight, output weights, start/end times)
- [ ] System calculates yield percentages (primary, trim, by-product as % of source)
- [ ] System calculates lbs per hour from timing data
- [ ] Admin can manage list of cutters
- [ ] Admin can manage list of species
- [ ] Director can view cutter performance summaries (avg yield %, avg lbs/hr)
- [ ] Director can view detailed batch records
- [ ] Director can export data to Excel/CSV

### Out of Scope

- Trends over time (charts, week-over-week comparisons) — deferred to v2
- Google Sheets integration — replaced by built-in dashboard + export
- Mobile app — web-based is sufficient for computer station use
- Login/authentication — simple access model, anyone can enter data
- Real-time data entry — batch entry after completion is sufficient

## Context

**Business environment:**
- Wholesale distribution and processing company
- Seafood and meat products
- 6-15 cutters on the cutting floor
- Director of Seafood oversees operations and reviews performance

**Yield breakdown:**
- Source weight: raw material input (net weight)
- Primary yield: fillets, portions — the main product
- Usable trim: sellable secondary cuts
- By-product: frames, heads, skins, waste — non-primary output

**Workflow:**
- Supervisor enters data at a dedicated computer station on the floor
- Entry happens after each batch is completed
- Data needs to be accessible daily by the director

**Performance metrics:**
- Yield % = (output weight / source weight) × 100 for each category
- Lbs/hour = source weight / (end time - start time)

## Constraints

- **Platform**: Web-based — runs in browser at floor computer station
- **Users**: Simple access model — no complex permissions required
- **Data**: Must support admin-managed lists for cutters and species

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Built-in dashboard over Google Sheets | Cleaner UX, no external dependencies, export covers reporting needs | — Pending |
| Calculate yields on submit | Immediate feedback, data integrity | — Pending |
| Admin-managed species/cutter lists | Controlled vocabulary, prevents data inconsistency | — Pending |

---
*Last updated: 2025-01-19 after initialization*
