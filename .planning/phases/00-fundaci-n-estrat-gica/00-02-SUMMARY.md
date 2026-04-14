---
phase: 00-fundaci-n-estrat-gica
plan: "02"
subsystem: documentation
tags: [prd, compliance, ley-21719, arco-plus, personas, requirements]
dependency_graph:
  requires: []
  provides: [docs/PRD.md]
  affects: [.planning/REQUIREMENTS.md]
tech_stack:
  added: []
  patterns: [10-section B2B SaaS PRD structure, proto-persona methodology, manual-first integration architecture]
key_files:
  created: [docs/PRD.md]
  modified: []
decisions:
  - "Proto-personas defined from market context — validated with first customers in Phase 1"
  - "Integration architecture documented as manual-first (v1) evolving to automated buk.cl OAuth (v2/Phase 3)"
  - "Out of scope table extended with multi-tenant, stack, and pricing exclusions not in REQUIREMENTS.md"
metrics:
  duration: "~3 minutes"
  completed: "2026-04-13"
  tasks_completed: 2
  files_created: 1
  lines_written: 355
requirements_fulfilled: [DOC-02, DOC-03]
---

# Phase 0 Plan 02: PRD.md — Product Requirements Document Summary

**One-liner:** Full 10-section PRD for ARCO Legal compliance platform with 3 proto-personas, 5 user flows, 24 functional requirements (v1), 9 NFRs, and manual-first integration architecture — all anchored to Ley 21.719.

## What Was Built

`docs/PRD.md` — 355-line Product Requirements Document covering:

1. **Overview / Problem Statement** — Ley 21.719 context (in force Dec 1, 2026), ARCO+ rights (6 rights), penalty regime (5K/10K/20K UTM + 2-4% revenue), operational problem, core value proposition, and legal basis for data collection from encargados de tratamiento
2. **Goals and Success Metrics** — Primary goal + 5 measurable v1 metrics each linked to a legal requirement
3. **User Personas** — 3 proto-personas (Operador de Compliance, Administrador/Buyer, Titular/Data Subject) with current workflows, key pains, success metrics, and explicit validation flags
4. **User Stories / Main Flows** — 5 flows (titular submits, operator manages, system alerts, manual data collection, admin onboards) with numbered steps and Ley 21.719 legal basis
5. **Functional Requirements** — 24 v1 requirements across 6 modules: INTAK-01–05, TRACK-01–05, WORK-01–05, INTG-01–04, AUDIT-01–04, AUTH-01–04; all IDs traceable to REQUIREMENTS.md
6. **Non-Functional Requirements** — 9 NFRs: audit immutability, Spanish interface, 2s dashboard load, 99.5% uptime, daily backups, meta-compliance with Ley 21.719, secure auth, 5-user concurrency, data minimization
7. **Integration Architecture** — Manual-first philosophy + legal basis (derecho de acceso, encargados de tratamiento) + v1 manual checklist flow (INTG-01) + v2 buk.cl OAuth flow (INTG-02/03/04) + future integrations (INTG-05/06/07) + decision criteria
8. **Out of Scope** — 8 explicit exclusions matching REQUIREMENTS.md plus multi-tenant, stack, and pricing
9. **Open Questions** — 4 questions: identity validation approach, PyME grace period confirmation, first client profile, hosting jurisdiction
10. **Assumptions** — 5 assumptions with explicit risk-if-wrong statements

## Commits

| Task | Name | Commit | Files |
|------|------|--------|-------|
| 1 | PRD Sections 1-5 | 707887f | docs/PRD.md (created, 215 lines) |
| 2 | PRD Sections 6-10 | 2da65b6 | docs/PRD.md (appended, +140 lines) |

## Deviations from Plan

None — plan executed exactly as written. All acceptance criteria met for both tasks on first attempt.

## Known Stubs

None. The PRD is a documentation artifact; all content is fully written. Functional requirement IDs marked as "v2 — Phase 3" (INTG-02/03/04) are intentionally deferred per REQUIREMENTS.md traceability — this is by design, not a stub.

## Threat Flags

None. `docs/PRD.md` is a Markdown document containing product requirements. No code, no data processing, no external services, no credentials. The threat model disposition `accept` (T-00-02) applies — document contains requirements, not secrets.

## Self-Check: PASSED

- `docs/PRD.md` exists: FOUND
- Task 1 commit 707887f: FOUND
- Task 2 commit 2da65b6: FOUND
- All 10 H2 sections present: VERIFIED
- All 24 v1 requirement IDs present: VERIFIED (INTAK-01–05, TRACK-01–05, WORK-01–05, INTG-01–04, AUDIT-01–04, AUTH-01–04)
- All 9 NFR IDs present: VERIFIED (NFR-01 through NFR-09)
- Ley 21.719 referenced 24 times: VERIFIED
- Document line count 355 (min 250): VERIFIED
