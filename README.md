<div align="center">

# GRC AI-GRC Knowledge Base

**Governance · Risk · Compliance**

Study notes, advisory engagements, GRC tooling, audit work, and AI governance research.
Focused on Saudi Arabian, Gulf, Indian, and international regulatory frameworks.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kayShahbaaz-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kayShahbaaz)
[![GitHub](https://img.shields.io/badge/GitHub-kayShahbaaz-181717?style=flat&logo=github)](https://github.com/kayShahbaaz)
[![Alias](https://img.shields.io/badge/Alias-kayn0x-00bfff?style=flat)](#)

</div>

---

## What's Here

| # | Section | What it contains |
|---|---|---|
| 1 | [Study Notes](#1-study-notes) | 11-module GRC curriculum + TryHackMe governance notes |
| 2 | [Advisory Portfolio](#2-advisory-portfolio) | 5 client engagements across India & Saudi Arabia, GRC Analyst → Auditor |
| 3 | [GRC Tooling](#3-compliance-tooling) | PDPL PII scanner, IAM audit engine, Islamic fintech GRC framework |
| 4 | [AI Governance](#4-ai-governance) | AI-GRC research paper + interactive compliance checker for Saudi/Gulf |

---

## Frameworks Covered

| Domain | Frameworks |
|---|---|
| Information Security | ISO/IEC 27001:2022 |
| Cybersecurity | NIST CSF, NCA ECC-1:2018, NCA ECC-2:2024 |
| Financial Sector | SAMA CSF, CMA |
| Privacy | GDPR, India DPDP Act 2023, Saudi PDPL |
| Trust & Compliance | SOC 2 (TSC) |
| AI Governance | ISO/IEC 42001:2023, NIST AI RMF, SDAIA AI Ethics, EU AI Act |
| Islamic Finance | AAOIFI Shariah Standards |
| Risk | ISO 31000, NIST SP 800-30, OCTAVE, FAIR |

---

## 1. Study Notes

### **[grc-notes](https://github.com/kayShahbaaz/grc-notes)**

An 11-module GRC curriculum written from the perspective of a practising GRC Analyst — not theory for its own sake, but how frameworks, regulations, and risk methodology actually work in real organizational environments.

| Module | Topic | Domain |
|---|---|---|
| 0 | GRC Core Concepts & Terminology — governance structures, risk lifecycle, control types, CIA triad, what a GRC Analyst does day to day | Foundation |
| 1 | ISO 27001 — mandatory clauses, Annex A controls, risk assessment, Statement of Applicability, certification and audit process | Information Security |
| 2 | NIST CSF — six core functions (Govern, Identify, Protect, Detect, Respond, Recover), implementation tiers, gap analysis usage | Cybersecurity |
| 3 | SOC 2 — five Trust Service Criteria, Type 1 vs Type 2 distinction, audit process, what auditors actually test | Trust & Compliance |
| 4 | GDPR + India DPDP Act — principles, lawful bases, eight data subject rights, DPDP Act 2023, direct comparison of where the two laws align and diverge | Privacy |
| 5 | NCA ECC — Saudi mandatory cybersecurity baseline, five domains, 114 controls, maturity model, relation to ISO 27001 | Saudi Cybersecurity |
| 6 | SAMA CSF — Saudi financial sector framework, four domains, maturity model, annual self-assessment cycle, interaction with NCA ECC | Saudi Banking Security |
| 7 | Saudi PDPL — principles, lawful bases, data subject rights, breach notification, Privacy Officer role, comparison with GDPR | Saudi Privacy |
| 8 | ISO 42001 — AI management system standard, AI-specific risk (bias, fairness, model drift, human oversight), what AI governance work looks like in practice | AI Governance |
| 9 | Risk Assessment Methods — qualitative vs quantitative, ALE/SLE/ARO formulas, NIST SP 800-30, ISO 31000, OCTAVE, FAIR, building a risk matrix, running an assessment end to end | Risk |
| 10 | GRC Tools — enterprise platforms (Archer, ServiceNow GRC, MetricStream), compliance automation (Vanta, Drata, Sprinto, Secureframe), agentic AI shift in compliance tooling (2025–2026) | Practical Skills |

---
### **[thm-governance-and-regulation](https://github.com/kayShahbaaz/thm-governance-and-regulation)**

Structured study notes from the TryHackMe Governance & Regulation room covering governance frameworks, documentation hierarchy (policies → standards → procedures → guidelines → baselines), and the regulatory landscape across GDPR, HIPAA, and PCI-DSS.

---

## 2. Advisory Portfolio

### **[resolute-compliance-advisory](https://github.com/kayShahbaaz/resolute-compliance-advisory) — GRC Advisory Portfolio**

Five client engagements delivered through Resolute Compliance Advisory LLP across two years, demonstrating full progression from GRC Analyst (implementation) to GRC Auditor (independent assurance). All client names anonymised. Engagements span Indian and Saudi regulatory frameworks.

| Engagement | Industry | Frameworks | Role | Key Finding |
|---|---|---|---|---|
| Brightpath | IT Services, Bengaluru | ISO 27001:2022 + SOC 2 | GRC Analyst | 37.6% ISO conformance (35/93 controls); former employee credentials live — Critical risk |
| Medlink | Healthtech, Mumbai | ISO 27001:2022 + GDPR + India DPDP Act | GRC Analyst | 49.5% ISO conformance; hardcoded AWS credentials in production — Critical risk; no GDPR Article 28 DPAs |
| Projects 3, 4, 3C | Saudi sectors (insurance, healthcare) | NCA ECC-1:2018, NCA ECC-2:2024, SAMA CSF | GRC Auditor | Independent audit and assurance across Saudi NCA regulatory framework |

Deliverables per engagement include: engagement letter, gap assessment report, Statement of Applicability, risk register, remediation roadmap with Gantt chart and dashboard, executive summary — all formatted as client-facing professional documents.

---

## 3. GRC Tooling


### **[pdpl-pii-scanner](https://github.com/kayShahbaaz/pdpl-pii-scanner) — Saudi PDPL Compliance Tool**

Python tool that scans CSV and Excel files for Saudi PII, classifies every finding into PDPL's legal tiers, risk-scores each one, checks for governance gaps, and produces redacted copies. Output: bilingual EN/AR interactive HTML dashboard + CSV/console reports.

Detects 8 PII types across PDPL's three legal tiers:

| PII Type | PDPL Tier | Obligation |
|---|---|---|
| National ID, Iqama, mobile, passport, email, address | Personal Data | Standard consent and protection obligations |
| IBAN / bank account | Credit Data (Article 24) | Enhanced protections for financial data |
| Health/medical, religious/political affiliation | Sensitive Data (Article 1(11)) | Explicit consent + DPIA required |

Detection uses layered confidence scoring (High/Medium/Low) across regex pattern matching, validation rules, and column name hints — not a flat yes/no. Also flags governance gaps: missing consent tracking and cross-border transfer signals. Built on PDPL Article 1 defined terms and SDAIA public guidance.
[Live demo](https://kayshahbaaz.github.io/pdpl-pii-scanner/)

---

### **[iam-risk-assurance](https://github.com/kayShahbaaz/iam-risk-assurance) — IAM Audit Engagement**

SQL-based IAM audit for Najm Financial Services Co. (~400 staff, Riyadh) — SAMA-regulated, subject to NCA ECC mandatory controls. July–November 2025. Seven checks across the full IAM lifecycle, 203 findings, overall IAM compliance score of 62% against a SAMA CSF target of ≥85%.

| # | Audit Check | Control Reference |
|---|---|---|
| 1 | Dormant accounts — no login in 90+ days | ISO A.9.2.5 / SAMA AC-3 / NCA IAM-3 |
| 2 | Orphaned accounts — terminated staff still active | ISO A.9.2.6 / SAMA AC-2 / NCA IAM-2 |
| 3 | Privileged account monitoring (PAM) | ISO A.9.4.4 / SAMA AC-6 / NCA IAM-5 |
| 4 | Segregation of duties violations | ISO A.9.2.3 / SAMA AC-5 / NCA IAM-4 |
| 5 | Excessive permissions / least privilege | ISO A.9.2.2 / SAMA AC-6 / NCA IAM-3 |
| 6 | JML process compliance (Joiner, Mover, Leaver) | ISO A.9.2.1 / SAMA AC-2 / NCA IAM-1 |
| 7 | Failed login anomalies / brute force detection | ISO A.9.4.2 / SAMA SI-3 / NCA IAM-6 |

203 findings: 23 critical · 47 high · 89 medium · 34 low. Most serious issues: orphaned accounts on critical systems for staff terminated months earlier; SoD conflicts in the Core Banking System allowing the same user to initiate and approve transactions; privileged accounts with no MFA on critical infrastructure. Audit database and all SQL detection queries built from scratch. Bilingual EN/AR dashboard with RTL toggle. Formal report delivered in both languages.
[Live dashboard](https://kayshahbaaz.github.io/iam-risk-assurance/)

---

### **[al-mizan](https://github.com/kayShahbaaz/al-mizan) — Shariah & Regulatory GRC for Islamic Fintech**

Most Islamic finance and fintech organisations run two disconnected compliance reviews — one for SAMA/CMA regulation, one for Shariah board approval. Al-Mizan runs both in a single unified workflow. Built for the Saudi Vision 2030 market.

Three modules in one interactive bilingual dashboard:

- **Governance** — maturity self-assessment scored simultaneously against regulatory governance requirements and Shariah governance principles
- **Risk** — Gharar Risk Matrix scoring each product category for uncertainty/ambiguity risk per AAOIFI Standard No. 31, with mitigation guidance per product type
- **Compliance** — dual-aspect audit checklist covering SAMA/CMA statutory requirements and Shariah board approval requirements in a single pass

Frameworks: SAMA CSF, CMA, Saudi PDPL, AAOIFI Shariah Standards. Fully interactive bilingual EN/AR with RTL layout switching. Self-contained, no server needed.
[Live dashboard](https://kayshahbaaz.github.io/al-mizan/)

---

## 4. AI Governance


### **[aigrc-imf](https://github.com/kayShahbaaz/aigrc-imf) — AI-GRC Integrated Management Framework**

Organisations across regulated Gulf industries are deploying AI in GRC functions — fraud detection, compliance monitoring, risk scoring, regulatory reporting — at a pace that has outrun the governance architectures meant to control them. The documented consequences: algorithmic bias in credit decisions, privacy violations under Saudi PDPL, adversarial manipulation of compliance models, and accountability gaps when AI-generated determinations go unchecked.

This repository contains two outputs:

**Academic paper** — proposes the AI-GRC Integrated Management Framework (AI-GRC IMF), a five-phase lifecycle governance model grounded in ISO/IEC 27001:2022 and ISO/IEC 42001:2023, cross-referenced against Saudi PDPL, SDAIA AI Ethics Principles, NCA ECC-1:2018, SAMA CSF, NIST AI RMF, and the EU AI Act.

**Interactive compliance checker** — organisations self-assess their AI systems against the AI-GRC IMF's five phases and receive a personalised AI-generated remediation report mapped to Saudi regulatory obligations. Open `index.html` in any browser — no installation, no server.

Frameworks: ISO/IEC 27001:2022, ISO/IEC 42001:2023, Saudi PDPL, SDAIA AI Ethics, NCA ECC-1:2018, SAMA CSF, NIST AI RMF, EU AI Act.
[Live dashboard](https://kayshahbaaz.github.io/aigrc-imf/)

---

### **[aigrc-audit-suite](https://github.com/kayShahbaaz/aigrc-audit-suite) — AI GRC Audit Suite**

Work in progress — details will be added on completion.

---

<div align="center">

Actively maintained — connect on [GitHub](https://github.com/kayShahbaaz)

</div>
