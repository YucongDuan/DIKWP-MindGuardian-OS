# DIKWP MindGuardian OS

**DIKWP MindGuardian OS** is an open-source, offline-first mental health navigation and safety-boundary system.

It is designed for personal reflection, community health navigation, clinician handoff preparation, peer-support triage, and non-diagnostic mental-health literacy. It converts user-provided notes, symptoms, stressors, protective factors, goals, consent boundaries, and access barriers into a DIKWP mental-health ledger and safety-oriented action package.

## Core Position

MindGuardian is **not** a diagnostic system, therapist, emergency service, medical device, or substitute for licensed care. It does not prescribe medication, does not classify a person with a psychiatric disorder, and does not delay urgent care. Its purpose is to help people organize what they already know, detect red-flag boundaries, prepare questions, and escalate when safety risk appears.

If someone may be in immediate danger, contact local emergency services now. In the United States and some territories, the 988 Suicide & Crisis Lifeline can be called, texted, or chatted for crisis support; other countries should configure local crisis resources in `configs/default_policy.json`.

## Why DIKWP

Mental health is not only a symptom list. It is a field of data, meaning, history, body state, social constraint, value conflict, intent, stigma, and safety boundary. DIKWP provides a structured way to separate:

- **D / Data**: explicit observations, symptoms, sleep, stressors, protective factors.
- **I / Information**: patterns, triggers, time course, social relationships, access barriers.
- **K / Knowledge**: non-diagnostic risk interpretation and care-navigation knowledge.
- **W / Wisdom**: safety, dignity, privacy, culture, equity, stigma, and cost tradeoffs.
- **P / Purpose**: user goals, values, constraints, time horizon, and feedback loop.
- **R / Reliability**: source confidence, uncertainty, residuals, escalation conditions.

## Main Outputs

- `mindguardian_report.json`
- `dikwp_mental_health_ledger.json`
- `safety_boundary_plan.json`
- `clinician_handoff.md`
- `community_support_queue.csv`
- `privacy_consent_ledger.json`
- `recommendations.md`

## Install

```bash
pip install -e .
```

## Analyze One Profile

```bash
mindguardian analyze examples/sample_mental_health_profile.json --out outputs/demo
```

## Analyze a Community Batch

```bash
mindguardian batch examples/sample_community_batch.json --out outputs/demo
```

## Static Boundary Audit

```bash
mindguardian static-audit src --out outputs/demo/static_boundary_audit_report.json
```

## Streamlit UI

```bash
pip install -e .[app]
streamlit run src/dikwp_mindguardian/app.py
```

## Safety Boundary

This tool is intentionally designed as a **decision-preparation layer**, not an autonomous clinical authority. High-risk content is escalated; unsupported certainty is downgraded; privacy and consent are explicit; outputs are non-diagnostic.

## Attribution

This project is prepared for the DIKWP open-source ecosystem and includes attribution to Yucong Duan / DIKWP in `NOTICE` and `CITATION.cff`.
