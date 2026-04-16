# AI Transparency & Trustworthiness Assessment (ATTA)
## Framework Documentation — v3.1

**Document type:** Public transparency documentation

**Framework version:** ATTA v3.1

**Last updated:** April 2026 (v3.1)

**Status:** Active

---

## Contents

1. [Introduction](#1-introduction)
2. [Design Philosophy](#2-design-philosophy)
3. [What ATTA Evaluates — and What It Does Not](#3-what-atta-evaluates--and-what-it-does-not)
4. [Framework Structure — 6 Dimensions · 30 Criteria](#4-framework-structure--6-dimensions--30-criteria)
5. [The Scoring System](#5-the-scoring-system)
6. [Industry Profiles & Dimension Weighting](#6-industry-profiles--dimension-weighting)
7. [How Evaluations Are Conducted](#7-how-evaluations-are-conducted)
8. [Regulatory Basis](#8-regulatory-basis)
9. [Known Limitations](#9-known-limitations)
10. [Interpreting Scores](#10-interpreting-scores)
11. [Challenging a Score](#11-challenging-a-score)
12. [Intended Uses & Misuses](#12-intended-uses--misuses)
13. [Version History & Change Log](#13-version-history--change-log)
14. [Glossary](#14-glossary)

---

## 1. Introduction

The **AI Transparency & Trustworthiness Assessment (ATTA)** is an open evaluation framework for assessing AI vendors and AI SaaS platforms on the basis of what they *publicly disclose* about their AI systems, data practices, security posture, and governance structures.

ATTA does not evaluate the quality of an AI system's outputs, its commercial viability, user experience, or pricing. It evaluates a single, answerable question:

> **How much can an enterprise buyer know about this vendor's AI trustworthiness from publicly available information?**

The framework produces a structured score across 30 criteria in 6 dimensions, weighted by industry context. Scores are not verdicts on whether a vendor is safe, ethical, or compliant — they are measures of *public evidence quality* relative to a defined set of regulatory and governance standards.

### Who this document is for

This documentation is intended for:

- **Vendors being evaluated** — to understand exactly how scores are derived, what evidence improves them, and how to request a review
- **Enterprise buyers** using ATTA reports in procurement due diligence — to understand what the scores mean and how to apply them
- **Regulators and auditors** who may encounter ATTA reports in vendor documentation packages
- **Researchers and journalists** writing about AI vendor transparency and compliance
- **Anyone** who wants to understand the methodology before relying on a score

---

## 2. Design Philosophy

### Trustworthiness-first, not compliance-first

Earlier versions of this framework (v1.7, v2.0) were organised around the EU AI Act as the central principle. ATTA v3.0 is organised around **trustworthiness as an observable property** — then mapped to the regulations that demand or validate it.

The practical difference: a vendor who says "we comply with the EU AI Act" without any supporting evidence scores lower than a vendor who publishes model cards, red-team results, and a GDPR DPA — even if neither uses the words "EU AI Act" prominently. Evidence of trustworthy behaviour is what matters, not regulatory vocabulary.

### Public evidence only

ATTA scores are deliberately **bounded to publicly discoverable information**. This is a design choice, not a limitation to apologise for. An enterprise buyer conducting initial vendor due diligence can only act on what a vendor chooses to make public. Internal practices that are not documented or disclosed cannot be relied upon as safeguards.

This means:

- A vendor with excellent internal AI safety practices but poor public documentation will score lower than a vendor with strong public documentation
- A vendor with strong public documentation may have weaker internal practices than their score implies
- The score measures *transparency*, which is both a proxy for trustworthiness and a governance behaviour in its own right

### Regulation-anchored, not regulation-dependent

Each ATTA criterion maps to one or more specific regulatory obligations or international standards. This is not because compliance equals trustworthiness — it does not — but because regulations are the clearest publicly verifiable standard against which vendor behaviour can be assessed. The regulatory references tell evaluators *what to look for* and give vendors *a clear target to document against*.

### Designed to be contested

ATTA is not intended as a final word on any vendor's trustworthiness. It is designed to surface specific, evidenced gaps that can be investigated, challenged, and remediated. Every score includes a written justification citing the specific evidence found (or absent), enabling vendors to point to where the evaluator is wrong and procurement teams to know exactly what to request.

---

## 3. What ATTA Evaluates — and What It Does Not

### ✅ What ATTA evaluates

- Whether the vendor has publicly published documentation on each of 30 specific trustworthiness criteria
- The quality and verifiability of that documentation (marketing claim vs. named certification vs. downloadable audit report)
- Whether third-party evidence corroborates the vendor's own statements
- Whether the vendor's publicly stated practices align with applicable regulatory obligations
- How the vendor's transparency posture compares to the requirements of the industry sector in which they are being evaluated

### ❌ What ATTA does not evaluate

| What it doesn't assess | Why |
|:--|:--|
| **Actual internal security practices** | Internal controls are not publicly verifiable without an NDA and vendor cooperation |
| **AI output quality or accuracy** | ATTA evaluates whether accuracy is *disclosed* — not whether the disclosed accuracy is good enough for a specific use case |
| **Vendor financial stability or continuity** | Outside scope |
| **Contract terms, pricing, or SLAs** | Commercial, not transparency-related |
| **Whether the vendor is actually compliant with law** | Only regulators with enforcement powers can determine legal compliance |
| **Comparative rank-ordering** | A score of 70 for Vendor A and 68 for Vendor B does not mean A is a better vendor than B — it means A has somewhat better public documentation |
| **Whether a vendor is "safe" to use** | Safety is use-case specific; ATTA provides evidence for that judgment, not the judgment itself |

> [!WARNING]
> **ATTA scores are not compliance certificates.** A vendor scoring 90/100 may still be non-compliant with applicable law. A vendor scoring 40/100 may have excellent internal practices that simply aren't documented publicly. The score measures one thing: the quality and completeness of publicly available evidence across 30 criteria.

---

## 4. Framework Structure — 6 Dimensions · 30 Criteria

ATTA is organised into 6 regulatory dimensions, each containing 5 criteria. Each criterion is scored 0–5, giving a maximum of 25 points per dimension and 150 raw points in total. Industry-specific weights convert the raw dimension scores into a single 0–100 overall score.

### Dimension 1 — AI Trustworthiness & Safety

```
Regulatory Anchors: EU AI Act · ISO 42001 · NIST AI RMF · OECD AI Principles
```

This is the primary dimension. It assesses the core observable trustworthy AI behaviours — risk classification, safety testing, model documentation, incident transparency, and bias/fairness — with the EU AI Act as the primary regulatory anchor but evaluated as trustworthiness properties, not as a compliance checklist.

| ID | Criterion | What It Measures |
|:--|:--|:--|
| `AIT1` | **AI Risk Classification & EU AI Act Alignment** | Has the vendor publicly classified their AI under EU AI Act risk tiers? Is a rationale published? For GPAI providers: GPAI Code of Practice signatory status. For deployers: Article 26 compliance documentation. |
| `AIT2` | **Safety Testing, Red-Teaming & Adversarial Evaluation** | Is there documented evidence of safety testing, red-teaming, or adversarial evaluation before and after deployment? Are methodologies or results published? |
| `AIT3` | **Technical Documentation & Model Cards** | Are model cards or system cards published for production AI systems? Do they cover intended purpose, training data categories, performance metrics, known limitations, and out-of-scope uses? |
| `AIT4` | **Incident History, Known Failures & Limitations** | Does the vendor transparently disclose known AI limitations, historical safety incidents, or significant failure modes? Are post-incident analyses published? |
| `AIT5` | **Bias, Fairness & Non-Discrimination** | Are documented procedures for identifying and mitigating demographic and cultural bias published? Are fairness evaluation results or disaggregated performance metrics disclosed? |

---

### Dimension 2 — Data Protection & Privacy

```
Regulatory Anchors: GDPR · HIPAA · CCPA · ePrivacy Directive
```

Evaluates data privacy posture across GDPR compliance, data subject rights mechanisms, retention and deletion policies, cross-border transfer safeguards, and HIPAA alignment for healthcare-relevant deployments.

| ID | Criterion | What It Measures |
|:--|:--|:--|
| `DPP1` | **GDPR Compliance & DPA Availability** | Is GDPR compliance documented? Is a DPA available (self-service or on request)? Is a named DPO publicly identified? |
| `DPP2` | **Data Subject Rights Mechanisms** | Are all GDPR data subject rights (Articles 15–22) described with a clear submission process? Are response timelines stated? |
| `DPP3` | **Data Retention, Deletion & Minimisation** | Are specific retention periods published per data category? Is a deletion process documented? Are ZDR options mentioned? |
| `DPP4` | **Cross-Border Transfer Safeguards** | Are SCCs, BCRs, adequacy decisions, or DPF registrations documented? Is a sub-processor list published? |
| `DPP5` | **Healthcare Data & HIPAA Compliance** | Is a HIPAA BAA available? Are administrative, physical, and technical safeguards documented? *(Mark N/A if vendor does not process PHI.)* |

---

### Dimension 3 — Information Security

```
Regulatory Anchors: ISO/IEC 27001:2022 · SOC 2 Type II · NIS2 Directive · CSA STAR
```

Assesses the vendor's information security posture through third-party certifications, NIS2 alignment, vulnerability disclosure practices, and technical security controls.

| ID | Criterion | What It Measures |
|:--|:--|:--|
| `IS1` | **ISO/IEC 27001 Certification** | Is a current ISO 27001:2022 certificate held? Is it publicly downloadable with a defined scope covering the AI platform? |
| `IS2` | **SOC 2 Type II Attestation** | Has a SOC 2 Type II examination been completed, covering all five Trust Service Criteria? Is the report available to customers? |
| `IS3` | **NIS2 Directive Alignment** | Is NIS2 Article 21 compliance documented? Is NIS2 registration status disclosed? Are MFA, supply chain security, and incident reporting timelines evidenced? |
| `IS4` | **Vulnerability Disclosure & Incident Response** | Does a public VDP or bug bounty exist? Is a security contact identified? Are past advisories and remediation timelines published? |
| `IS5` | **Encryption, Access Controls & Security Architecture** | Are encryption standards (TLS version, AES-256), RBAC, MFA, and tenant isolation confirmed in public documentation? |

---

### Dimension 4 — AI Management & Governance

```
Regulatory Anchors: ISO/IEC 42001:2023 · EU AI Act Article 26 · NIST AI RMF
```

Evaluates AI-specific governance maturity — ISO 42001 certification, published risk frameworks, impact assessment processes, human oversight structures, and acceptable use enforcement.

| ID | Criterion | What It Measures |
|:--|:--|:--|
| `AMG1` | **ISO/IEC 42001 AI Management System** | Does the vendor hold ISO 42001:2023 certification? Is the certifying body and scope named? |
| `AMG2` | **AI Risk Framework & Responsible Scaling Policy** | Is a formal AI risk management framework published? Does it define thresholds, deployment conditions, and governance escalation? Is it versioned? |
| `AMG3` | **AI Impact Assessment & Risk Register** | Is an AI impact assessment process documented? Is a maintained AI risk register evidenced? Are customers given guidance for downstream risk assessments? |
| `AMG4` | **Human Oversight Mechanisms** | Are human oversight mechanisms described for AI operations? Is a named Responsible AI Officer or ethics board identified? Are escalation paths documented? |
| `AMG5` | **Acceptable Use Policy & Prohibited Applications** | Is there a specific AUP that explicitly prohibits harmful applications including EU AI Act Article 5 prohibited practices? Is it enforced with a documented violations process? |

---

### Dimension 5 — Sector-Specific Compliance

```
Regulatory Anchors: DORA · PCI DSS v4.0 · ISO 13485 · FedRAMP · NIS2 Annex I
```

Evaluates compliance with regulations specific to the vendor's target industries. Criteria not applicable to the vendor's scope are scored `N/A (0)` and do not penalise the overall score — the dimension weight accounts for this.

| ID | Criterion | Applicable Sector |
|:--|:--|:--|
| `SSC1` | **DORA / Financial Digital Resilience** | Financial services — banks, insurers, payment processors |
| `SSC2` | **PCI DSS / Payment Data Security** | Any vendor processing or enabling payment card data |
| `SSC3` | **Healthcare / Medical AI Compliance** | Healthcare, life sciences, medical device software |
| `SSC4` | **Critical Infrastructure & NIS2 Sector Obligations** | Energy, transport, water, digital infrastructure |
| `SSC5` | **Government & Public Sector Security** | Government agencies, public administration, law enforcement |

---

### Dimension 6 — Transparency & Accountability

```
Regulatory Anchors: EU AI Act Articles 13–15 · EU AI Act Annex IV · Stanford FMTI
```

Assesses the depth of public transparency around training data composition, performance benchmarks and limitations, audit trail capabilities, independent AI safety evaluations, and post-market monitoring.

| ID | Criterion | What It Measures |
|:--|:--|:--|
| `TAC1` | **Training Data Disclosure & Copyright Policy** | Is training data composition (categories, sources, date ranges) documented? Is a copyright / opt-out policy published? |
| `TAC2` | **Performance Benchmarks, Metrics & Limitations** | Are quantitative performance metrics published, including disaggregated subgroup performance? Are known failure modes documented? |
| `TAC3` | **Audit Logs, Explainability & Logging** | Are customer-accessible audit logs of AI decisions provided? Are explainability tools available? Are audit logs tamper-resistant? |
| `TAC4` | **Third-Party AI Safety Evaluations** | Has the AI system undergone independent evaluation for AI safety or fairness (beyond IT security audits)? Are results disclosed? |
| `TAC5` | **Changelog, Versioning & Post-Market Monitoring** | Is a public changelog maintained? Is a post-market monitoring programme documented? Are customers notified of material model changes? |

---

## 5. The Scoring System

### Per-criterion scores (0–5)

Every criterion is scored on a 0–5 integer scale:

| Score | Label | Standard of Evidence Required |
|:--:|:--|:--|
| **5** | ⭐ Full marks | Comprehensive and independently verifiable. A publicly downloadable third-party audit certificate, a named certifying body with a defined scope, a regulatory body confirmation, or quantitative evidence that a reviewer can independently check without contacting the vendor. |
| **4** | ✅ Strong | Clear policy with verifiable evidence. A named certification, a linked audit report (even if under NDA), specific quantitative metrics, or a named officer/team with a public contact. The evaluator can verify that the claim is substantiated. |
| **3** | 🔵 Moderate | Clear policy that addresses the requirement, but with no independently verifiable implementation evidence. The vendor describes what they do but provides no external confirmation that they do it. |
| **2** | 🟡 Developing | Some relevant policy exists but is incomplete, generic, outdated, or lacks external validation. A vague reference to a regulation without describing the vendor's specific approach. |
| **1** | 🟠 Weak | Vague or aspirational statements only. Marketing language about commitment to the topic with no concrete policy, process, or certification evidence. |
| **0** | ❌ Absent / N/A | No relevant information found in publicly available documentation, or the criterion is genuinely not applicable to this vendor's scope and the evaluator has confirmed this. |

### The N/A distinction

A score of **0** covers two different situations:

1. **Absent** — The requirement applies but the vendor has published nothing on the topic
2. **Not Applicable** — The requirement genuinely does not apply (e.g., `DPP5` HIPAA for a vendor that does not process health data)

Evaluators are expected to distinguish between these in their written justification. Both produce a raw score of 0, but the `N/A` case does not reflect a transparency failure.

### Dimension scores

Each dimension's score is calculated as a percentage of points achieved against points possible:

```
Dimension Score (%) = (Sum of criterion scores in dimension) / (Sum of max scores in dimension) × 100
```

For a dimension with 5 criteria (max 5 points each = 25 points max):

```
Dimension Score = (achieved points / 25) × 100
```

### Overall weighted score

The overall score is the weighted sum of dimension percentage scores, applying the industry profile weights:

```
Overall Score = Σ (Dimension Score × Applied Industry Weight)
```

Because all dimension weights sum to 1.0 (100%), the overall score is always in the range 0–100.

**Example calculation (General Technology profile):**

| Dimension | Raw Score | % | Industry Weight | Contribution |
|:--|:--:|:--:|:--:|:--:|
| AI Trustworthiness & Safety | 12/25 | 48.0% | 20% | 9.6 |
| Data Protection & Privacy | 15/25 | 60.0% | 20% | 12.0 |
| Information Security | 18/25 | 72.0% | 20% | 14.4 |
| AI Management & Governance | 12/25 | 48.0% | 20% | 9.6 |
| Sector-Specific | 1/25 | 4.0% | 5% | 0.2 |
| Transparency & Accountability | 10/25 | 40.0% | 15% | 6.0 |
| **TOTAL** | | | **100%** | **51.8** |

### Rating thresholds

| Range | Maturity | Evidence Character | Procurement Implication |
|:--:|:--|:--|:--|
| 80–100 | ⭐ **Advanced** | Comprehensive, multi-source, third-party-verified evidence across most dimensions. Vendor proactively publishes documentation with external corroboration. | Standard due diligence. Verify named certifications directly with issuing bodies. |
| 60–79 | 🔷 **Established** | Substantiated documentation with independently verifiable evidence in core areas. Identifiable gaps in one or two dimensions. | Request evidence packages for the specific gap criteria before finalising selection. |
| 40–59 | 🔶 **Developing** | Partial evidence across key dimensions. Some verifiable disclosures alongside unsubstantiated statements or documentation gaps. | Request documentation packages for all criteria below 3/5. Verify certifications directly. Vendor meeting recommended. |
| 0–39 | 🌱 **Emerging** | Limited public documentation. Significant investment in transparency infrastructure needed. May reflect an early-stage vendor or one that has not yet prioritised public disclosure. | Significant due diligence required. Request direct evidence package and internal documentation before use in any regulated context. |

---

## 6. Industry Profiles & Dimension Weighting

The same vendor evaluated under different industry profiles will receive different overall scores. This is intentional: a vendor's transparency posture is only meaningful relative to what their customers actually need.

A social media SaaS platform with excellent ISO 27001 documentation but no HIPAA BAA is an appropriate vendor for retail brands and a problematic vendor for a hospital. The profile-weighted score communicates this contextual suitability.

### Profiles at a glance

| Profile | Icon | Key Priority | Sector-Specific Weight |
|:--|:--:|:--|:--:|
| `healthcare` | 🏥 | AI Trustworthiness + Data Protection | 15% |
| `finance` | 🏦 | Information Security + Sector (DORA/PCI DSS) | 20% |
| `critical_infrastructure` | ⚡ | Information Security (highest weight) | 20% |
| `public_sector` | 🏛️ | AI Trustworthiness (highest weight) | 15% |
| `insurance` | 🛡️ | AI Trustworthiness + AI Governance (bias focus) | 15% |
| `general_tech` | 💻 | All dimensions balanced | 5% |

### Full weight matrix

The table below shows the dimension weight applied to each score under each industry profile:

| Dimension | 🏥 Healthcare | 🏦 Finance | ⚡ Infra | 🏛️ Public | 🛡️ Insurance | 💻 General |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|
| AI Trustworthiness & Safety | **25%** | 20% | 20% | **30%** | **25%** | 20% |
| Data Protection & Privacy | **25%** | 15% | 10% | 20% | 20% | 20% |
| Information Security | 15% | **20%** | **30%** | 15% | 15% | 20% |
| AI Management & Governance | 15% | 15% | 15% | 15% | **20%** | 20% |
| Sector-Specific Compliance | **15%** | **20%** | **20%** | **15%** | **15%** | 5% |
| Transparency & Accountability | 5% | 10% | 5% | 5% | 5% | **15%** |
| **Total** | **100%** | **100%** | **100%** | **100%** | **100%** | **100%** |

### Critical criteria

Each profile designates a subset of criteria as **critical** — the highest-priority gaps for that sector. These are flagged prominently in reports and should be the first focus of remediation for vendors serving that industry.

| Profile | Critical Criteria |
|:--|:--|
| 🏥 Healthcare | `AIT1` `AIT2` `AIT3` `DPP5` `SSC3` `AMG4` |
| 🏦 Finance | `AIT1` `AIT5` `IS2` `IS3` `SSC1` `SSC2` `AMG3` |
| ⚡ Critical Infrastructure | `AIT1` `AIT2` `IS3` `IS4` `IS5` `SSC4` `AMG2` |
| 🏛️ Public Sector | `AIT1` `AIT3` `AIT5` `DPP1` `DPP2` `SSC5` `AMG4` `TAC3` |
| 🛡️ Insurance | `AIT1` `AIT5` `AMG3` `AMG5` `DPP1` `SSC1` |
| 💻 General Tech | `AIT1` `AIT3` `DPP1` `DPP3` `IS1` `IS2` `AMG1` `TAC1` |

---

## 7. How Evaluations Are Conducted

ATTA evaluations follow a four-stage process. Understanding each stage helps readers assess the reliability of any individual report.

### Stage 1 — URL Discovery

A crawler performs a breadth-first search of the vendor's public web presence, seeded with the vendor's primary domain. Pages are scored by keyword density against a list of regulatory and trustworthiness signals — terms like "ISO 27001", "GDPR", "model card", "red team", "EU AI Act", "data protection officer", and so on. Pages meeting a minimum keyword threshold are collected for scraping.

**What this can miss:**
- Documentation that is behind a login wall, NDA, or access request
- PDF documents not indexed by the vendor's own sitemap
- Information published only in press releases on third-party sites
- Certifications listed only in image format (not as text)
- Video or webinar content describing policies

**Implication for scores:** A vendor who publishes their security page as a JavaScript-rendered single-page application without server-side rendering may have that page missed by the crawler. Evaluators should supplement automated crawling with manual review of known pages (trust center, legal, AI policy, security).

### Stage 2 — Content Scraping

Discovered URLs are scraped for their text content. PDFs linked from HTML pages are extracted as text. The content is consolidated into a single structured evidence corpus, preserving source URLs for citation.

**Quality considerations:**
- Content is captured at a point in time. Vendor documentation changes — a score from six months ago may not reflect current documentation
- Rendering issues, paywalls, or bot-detection systems can cause pages to return partial or no content

### Stage 3 — LLM-Assisted Criterion Scoring

Each of the 30 criteria is evaluated by an LLM (default: `gemini-2.5-flash`) acting as an AI Transparency & Trustworthiness Analyst. The LLM receives:

- The full consolidated evidence corpus with source URLs preserved
- The criterion definition, description, keywords, and regulatory references
- The industry context (profile name and display name)
- The 0–5 scoring rubric
- Instructions to cite specific evidence with source URLs and direct quotes

The LLM returns a structured JSON object per criterion: `{"score": N, "justification": "...", "evidence": [{"url": "...", "quote": "..."}]}`.

**Known LLM scoring characteristics and mitigations:**

| Risk | Mitigation |
|:--|:--|
| **Hallucinated evidence** — the LLM invents a quote or URL that does not exist | Every reported quote and URL should be independently verified against the source. Reports include direct hyperlinks for this purpose. |
| **Overconfidence on partial evidence** — scoring 4 when only marketing language is present | The rubric explicitly distinguishes marketing claims (1–2) from verifiable evidence (4–5). The LLM persona is instructed to be conservative. |
| **Missing context** — the LLM misses a relevant page not in the scraped corpus | Evaluators should supplement LLM scoring with manual review for high-stakes evaluations |
| **Score inconsistency across runs** — the same vendor scored on different days may receive slightly different scores | The JSON output format and structured rubric reduce but do not eliminate variance. Material decisions should request a human review |
| **Anchoring to vendor framing** — if a vendor uses compliance vocabulary extensively, the LLM may give credit for claims without evidence | The rubric instructs the LLM to distinguish between claims and verifiable evidence. Human review is the backstop for this. |

### Stage 4 — Report Generation

Criterion scores, justifications, and evidence are assembled into the evaluation report JSON. The `reporter.py` script generates either an HTML or native markdown report from this JSON. Both formats include all 30 criterion justifications with evidence citations, enabling independent verification of every score.

---

## 8. Regulatory Basis

ATTA draws on the following regulatory instruments and standards as evaluation anchors. This list defines the legal and normative framework within which evidence is assessed.

### Primary regulation

| Regulation | Jurisdiction | Relevance to ATTA |
|:--|:--|:--|
| **EU AI Act** (Regulation 2024/1689) | European Union | Primary regulatory anchor for Dimension 1 (AIT1–AIT5). Deployer obligations (Art. 26), GPAI obligations (Arts. 52–55), transparency (Arts. 13–15), technical documentation (Annex IV), systemic risk (Art. 55). |
| **GDPR** (Regulation 2016/679) | European Union | Primary anchor for Dimension 2 (DPP1–DPP4). Controller/processor obligations (Art. 28), DPO (Art. 37), data subject rights (Arts. 15–22), cross-border transfers (Arts. 44–49), DPIA (Art. 35). |
| **NIS2 Directive** (Directive 2022/2555) | European Union | Primary anchor for IS3 and SSC4. Article 21 security requirements, Article 23 incident reporting, Annex I/II sector classification. |
| **DORA** (Regulation 2022/2554) | European Union | Primary anchor for SSC1. ICT risk management, TLPT, third-party ICT provider requirements for financial sector. |
| **HIPAA** (45 CFR Parts 160 & 164) | United States | Primary anchor for DPP5 and SSC3. BAA requirements, safeguard obligations, PHI handling. |
| **CCPA** (California Civil Code §1798.100+) | United States (California) | Referenced in DPP2 and DPP3. Consumer rights over personal information. |

### Standards

| Standard | Body | Relevance |
|:--|:--|:--|
| **ISO/IEC 27001:2022** | ISO/IEC | Primary anchor for IS1. Information Security Management System (ISMS) certification. |
| **ISO/IEC 42001:2023** | ISO/IEC | Primary anchor for AMG1. AI Management System (AIMS) certification — the first international standard specifically for AI management. |
| **ISO/IEC 27017:2015** | ISO/IEC | Referenced in IS1. Cloud-specific security controls extending ISO 27001. |
| **ISO/IEC 27018:2019** | ISO/IEC | Referenced in IS1. Protection of PII in public cloud computing. |
| **SOC 2 (AICPA Trust Services Criteria 2017)** | AICPA | Primary anchor for IS2. Security, Availability, Confidentiality, Processing Integrity, and Privacy attestation. |
| **ISO 13485:2016** | ISO | Referenced in SSC3. Quality management systems for medical devices including SaMD. |
| **PCI DSS v4.0** | PCI Security Standards Council | Primary anchor for SSC2. Payment card data security. |
| **FedRAMP** | US GSA | Referenced in SSC5. US federal government cloud security authorisation. |

### Frameworks and guidance

| Framework | Body | Relevance |
|:--|:--|:--|
| **NIST AI RMF** (AI 100-1) | NIST (US) | Referenced in Dimensions 1 and 4. GOVERN, MAP, MEASURE, MANAGE functions inform AI risk framework evaluation. |
| **Stanford Foundation Model Transparency Index (FMTI)** | Stanford HAI | Referenced in TAC2 and TAC4. 100-indicator transparency index for foundation model providers. |
| **OECD AI Principles** | OECD | Referenced in Dimension 1. Five principles for responsible stewardship of trustworthy AI. |
| **GPAI Code of Practice** | EU AI Office | Referenced in AIT1. Voluntary code for GPAI model providers under EU AI Act. |
| **EU-US Data Privacy Framework** | US/EU | Referenced in DPP4. Legal basis for EU-US personal data transfers. |

---

## 9. Known Limitations

This section exists because transparency about limitations is itself a trustworthiness property. Any evaluation system that does not acknowledge its own limitations should be treated with additional scepticism.

### Limitation 1 — The documentation gap

**What it is:** A vendor's public documentation is a curated representation of their practices, not a complete picture. Vendors control what they publish. A sophisticated vendor with poor practices can score well by publishing detailed but unverified documentation. A vendor with excellent practices but a minimal public presence will score poorly.

**What this means for users:** ATTA scores should be treated as a starting point for due diligence, not a conclusion. High-stakes decisions require requesting vendor evidence packages, NDA-protected audit reports, and direct conversations with the vendor's security and governance teams.

**What ATTA does to mitigate this:** The rubric explicitly distinguishes between claims and verifiable evidence. Marketing language scores 1–2. Only named certifications, downloadable audit reports, and independently verifiable evidence scores 4–5. The structure of the rubric makes gaming through vague claims relatively expensive — it requires genuine documentation investment to score above 3 on any criterion.

---

### Limitation 2 — Currency

**What it is:** AI vendor documentation changes continuously. A certification may lapse, a DPO may resign, a trust center page may be restructured. ATTA reports reflect a snapshot of publicly available documentation at the time of evaluation.

**What this means for users:** Evaluate the date prominently displayed on every ATTA report. Reports older than 6 months should be treated with caution for fast-moving vendors. Certifications like ISO 27001 and SOC 2 should be independently verified against the issuing body's public registry.

**What ATTA does to mitigate this:** Every evidence citation includes a direct URL that evaluators and readers can visit to verify currency. The `TAC5` criterion (Changelog & Post-Market Monitoring) directly assesses whether vendors communicate material changes to their documentation.

---

### Limitation 3 — Language and geography

**What it is:** ATTA evaluations are primarily conducted on English-language documentation. Vendors whose primary documentation is in other languages (German, French, Japanese, Czech, etc.) may have more complete documentation in their native language than what is accessible to English-language crawlers and LLM evaluation.

**What this means for users:** For vendors headquartered in non-English-speaking countries, ATTA scores may understate the quality of their governance documentation. Buyers evaluating such vendors should request translated documentation summaries directly.

**What ATTA does to mitigate this:** This limitation is acknowledged in the evaluator guidance. Evaluators are instructed to note when a vendor appears to have multilingual documentation and to flag this as context in the report.

---

### Limitation 4 — N/A scoring in sector-specific criteria

**What it is:** Dimension 5 (Sector-Specific Compliance) contains criteria that are not applicable to most vendors. A general SaaS platform genuinely does not need DORA compliance or a HIPAA BAA. When criteria are scored N/A (0), they reduce the dimension's point total to near zero regardless of the platform — making the Sector-Specific dimension a poor discriminator for general-purpose vendors.

**What this means for users:** The very low Sector-Specific dimension score for general-purpose vendors (often 4–8%) is structural, not a sign of regulatory failure. The dimension weight for `general_tech` is deliberately set at 5% to limit its impact on the overall score. For sector-specific evaluations, this dimension becomes more meaningful because more criteria become applicable.

---

### Limitation 5 — LLM scoring variance

**What it is:** LLM-generated scores are not perfectly reproducible. Running the same evaluation on the same content corpus on two different days may produce scores that differ by 1–3 points on individual criteria, resulting in overall score differences of up to ±5 points.

**What this means for users:** Treat individual criterion scores as estimates, not measurements. The directional finding (this criterion is a gap; that one is strong) is more reliable than the precise numeric score. For criteria where the score significantly affects a procurement decision, commission a human expert review.

**What ATTA does to mitigate this:** The structured JSON output format, explicit rubric, and instruction to cite specific evidence all reduce but do not eliminate variance. The framework is designed so that the *justification* is as important as the *score* — a score without a readable justification and cited evidence is not a valid ATTA score.

---

### Limitation 6 — This framework does not assess AI output safety

**What it is:** ATTA does not evaluate whether a vendor's AI model is safe, accurate, unbiased, or appropriate for any specific use case. It assesses whether the vendor has *disclosed* their safety testing, accuracy, and bias evaluation — not whether those properties are at an acceptable level.

**What this means for users:** A vendor scoring 5/5 on `AIT2` (Safety Testing) has published extensive documentation about their red-teaming methodology. This does not mean their AI system is safe for your specific use case — only that they are transparent about their testing. The *content* of what is disclosed — the actual red-team results, the specific accuracy figures, the identified failure modes — requires separate expert assessment against use-case requirements.

---

## 10. Interpreting Scores

### The score as a procurement signal, not a verdict

The most useful way to read an ATTA score is not as a grade but as a set of specific, actionable questions to put to the vendor.

A score of **2/5 on `DPP3`** (Data Retention & Deletion Policies) means: *"We could not find published specific retention periods for each data category in your public documentation. Please provide your data retention schedule and confirm whether a Zero Data Retention option is available for enterprise customers."*

This is far more actionable than "this vendor scored 49/100."

### Absolute vs. relative interpretation

**Absolute interpretation:** The rating thresholds (Strong/Moderate/Weak/Very Weak) provide a context-independent reading. A score of 49/100 (Weak) signals that material documentation gaps exist and that significant due diligence is warranted before use in regulated contexts. This is true regardless of what other vendors in the same category score.

**Relative interpretation:** Comparing ATTA scores across vendors is valid *only* when the same industry profile and the same evaluation date are used. A Healthcare-profile score of 65 and a General Tech-profile score of 65 are not comparable — they reflect completely different weighting schemes.

### What a high score does not guarantee

A strong ATTA score (`≥80`) means:
- The vendor invests significantly in public documentation of their AI governance, security, and privacy practices
- Multiple statements are backed by independently verifiable third-party evidence
- The vendor's transparency posture is compatible with regulated enterprise procurement expectations

A strong score does **not** mean:
- The vendor is legally compliant with all applicable regulations
- The vendor's AI system is safe or appropriate for your specific use case
- The vendor's internal practices are as strong as their documentation implies
- The vendor will not experience a security incident or AI system failure
- The vendor's documentation will remain current

---

## 11. Challenging a Score

Any vendor who believes their ATTA score is inaccurate — because the evaluator missed published documentation, misinterpreted evidence, or cited a page that has since been updated — has a straightforward path to challenge specific criterion scores.

### What a valid challenge looks like

A valid challenge identifies:

1. The specific criterion ID (e.g., `AMG1`) being challenged
2. The URL of publicly available documentation the evaluator missed or misread
3. A brief explanation of why the cited documentation satisfies the criterion definition at a specific score level
4. Confirmation that the documentation was publicly available *at the time of the original evaluation*

### What is not a valid challenge

- Asserting that internal practices exceed what is documented publicly (internal practices are out of scope)
- Providing documentation that was published *after* the evaluation date
- Requesting score increases for documentation that exists behind a login, NDA, or access request (at evaluation time)
- Disagreeing with the framework's regulatory mapping without providing an alternative interpretation of the cited regulatory text

### Recalibration

When a valid challenge is submitted with new evidence, the specific criterion score may be revised upward. The overall score is recalculated using the corrected criterion score. The report is updated with a revision date, the previous score, the new score, and a note describing what new evidence was considered.

---

## 12. Intended Uses & Misuses

### ✅ Intended uses

- **Initial vendor screening** — quickly identifying which dimensions require deeper due diligence before investing in full vendor evaluation
- **Procurement checklist generation** — using low-scoring criteria as the basis for a vendor evidence request list
- **Comparative context** — understanding how a specific vendor's public documentation compares to general expectations for their industry
- **Vendor self-assessment** — vendors using ATTA criteria as a roadmap for which documentation to publish or improve
- **Research and journalism** — understanding the state of AI vendor transparency across an industry segment
- **Regulatory benchmarking** — mapping vendor documentation postures against specific regulatory obligations

### ❌ Misuses this documentation explicitly warns against

- **Publishing ATTA scores as compliance certificates** — ATTA scores are not evidence of regulatory compliance. Representing them as such to customers, regulators, or auditors is misleading.
- **Using a single ATTA score to make a final vendor selection decision** — the score is a starting point for due diligence, not a conclusion.
- **Comparing scores across different industry profiles** — a vendor's Healthcare score and their General Tech score are not comparable.
- **Using ATTA to make claims about AI system safety** — the framework assesses *disclosure of safety practices*, not the safety of AI outputs.
- **Treating an outdated report (>6 months old) as current** — documentation changes; verify currency of critical certifications directly.
- **Using ATTA to evaluate vendors for high-risk AI deployments without supplementing with human expert review** — for medical AI, financial credit decisioning, law enforcement AI, or other high-risk applications, ATTA is one input among several that expert assessors should review.

---

## 13. Version History & Change Log

### v3.1 — April 2026 (current)

**Evidence Maturity label system replaces binary quality labels:**

Previous versions used Strong / Moderate / Weak / Very Weak as overall and dimension rating labels. These implied a quality judgment on the vendor rather than on the *documentation posture* being assessed. v3.1 replaces these with an Evidence Maturity model — Emerging / Developing / Established / Advanced — to more accurately communicate what ATTA scores actually measure: the maturity of publicly available documentation evidence, not a verdict on the vendor.

**What changed:**

| Component | v3.0 | v3.1 |
|:--|:--|:--|
| Overall rating (0–100) | Strong / Moderate / Weak / Very Weak | Advanced / Established / Developing / Emerging |
| Dimension rating | Same 4-tier labels | Same 4 maturity tiers |
| Per-criterion labels (0–5) | Full marks / Strong / Moderate / Developing / Weak / Absent | Independently Verified / Evidenced / Documented / Referenced / Mentioned / Absent |
| Alert thresholds | `<25` critical, `<50` warning | `<40` Emerging alert, `<60` Developing alert |
| Emoji set | 🟢🟡🟠🔴 | ⭐🔷🔶🌱 |
| `scorer.py` console | Text labels | Emoji + maturity label per dimension |
| `reporter.py` heatmap tier labels | "Weak / Developing / Moderate / Strong" | "Minimal Evidence / Partial / Substantiated / Verified" |

All dimension weights, criterion definitions, and scoring rubric thresholds (0–5) are unchanged. Version bump from 3.0 → 3.1 only.

---

### v3.0 — April 2026

**Framework name change:** "EU AI Act Regulatory Compliance Framework" → "AI Transparency & Trustworthiness Assessment (ATTA)"

**Dimension 1 redesigned:**

| v2.0 | v3.0 | Reason |
|:--|:--|:--|
| *EU AI Act Conformity* (EUA1–EUA5) | *AI Trustworthiness & Safety* (AIT1–AIT5) | EU AI Act repositioned as one regulatory anchor rather than the organising principle. Trustworthiness behaviours evaluated directly. |
| EUA2: Conformity Assessment | AIT2: Safety Testing & Red-Teaming | Safety testing is the core trustworthiness evidence; conformity assessment is a regulatory procedure that may or may not reflect actual safety testing. |
| EUA4: GPAI Model Obligations | AIT4: Incident History & Known Failures | GPAI obligations are now reflected in AIT1; incident transparency is a distinct and more broadly applicable trustworthiness criterion. |
| EUA5: Systemic Risk Management | AIT5: Bias, Fairness & Non-Discrimination | Systemic risk (Article 55) is a GPAI-model-only obligation; bias/fairness applies to all AI vendors and is a higher-impact trustworthiness property. |

**Transparency dimension rebalanced:**

| v2.0 | v3.0 |
|:--|:--|
| TAC1: Model Card Publication | TAC1: Training Data Disclosure & Copyright Policy |
| TAC2: Training Data Disclosure | TAC2: Performance Benchmarks, Metrics & Limitations |
| TAC3: Performance Disclosure | TAC3: Audit Logs, Explainability & Logging |
| TAC4: Audit Logs & Explainability | TAC4: Third-Party AI Safety Evaluations |
| TAC5: Third-Party Audits | TAC5: Changelog, Versioning & Post-Market Monitoring |

Training data disclosure moved to TAC1 (first transparency criterion) reflecting its growing regulatory importance. Post-market monitoring added as TAC5 reflecting EU AI Act Article 72 requirements.

**AMG5 redesigned:** v2.0 "Bias & Fairness Policy" moved to Dimension 1 as AIT5. AMG5 becomes "Acceptable Use Policy & Prohibited Applications" — covering EU AI Act Article 5 prohibited practices.

**Technical improvements:**
- `scorer.py`: Added `--concurrency N` semaphore (default 5 parallel LLM calls)
- `scorer.py`: Added `--model` flag for runtime model selection
- `scorer.py`: Console Unicode progress bar per dimension at completion
- `reporter.py`: Unified dual-format output — `--format html` or `--format markdown`
- `reporter.py`: Native markdown generator produces zero external HTTP requests (no shields.io)
- `industry_profiles.json`: All `eu_ai_act` weight keys renamed to `ai_trustworthiness`
- Report JSON: Added `framework_abbrev`, `overall_rating`, and `dimension_summary` fields

---

### v2.0 — January 2026

- Introduced industry-specific dimension weighting (6 profiles: healthcare, finance, critical_infrastructure, public_sector, insurance, general_tech)
- Expanded from 20 criteria (v1.7) to 30 criteria across 6 dimensions
- Added Sector-Specific Compliance dimension (SSC1–SSC5) covering DORA, PCI DSS, ISO 13485, FedRAMP, NIS2 sector obligations
- Introduced `critical_criteria` flagging system per industry profile
- Added `is_critical` flag per criterion in the evaluation report JSON
- Replaced single-dimension EU AI Act assessment with multi-dimension framework

---

### v1.7 — September 2025

- Original framework release
- 4 dimensions, 20 criteria
- Single weighting scheme (no industry profiles)
- EU AI Act as primary organising framework
- HTML report output only

---

## 14. Glossary

**ATTA** — AI Transparency & Trustworthiness Assessment. The name of this evaluation framework.

**AIT / DPP / IS / AMG / SSC / TAC** — Criterion ID prefixes for each of the six dimensions: AI Trustworthiness (AIT), Data Protection & Privacy (DPP), Information Security (IS), AI Management & Governance (AMG), Sector-Specific Compliance (SSC), Transparency & Accountability (TAC).

**AUP (Acceptable Use Policy)** — A publicly published document specifying which uses of an AI system are permitted and which are prohibited.

**BAA (Business Associate Agreement)** — A contract required under HIPAA between a covered entity and a business associate that will process Protected Health Information on their behalf.

**CCPA** — California Consumer Privacy Act. US state privacy law granting California residents rights over their personal information.

**Critical criteria** — The subset of ATTA criteria designated as highest priority for a specific industry profile. Flagged prominently in reports and the first focus of remediation.

**DORA** — Digital Operational Resilience Act (Regulation 2022/2554). EU regulation mandating ICT risk management and resilience testing for financial entities, effective January 2025.

**DPA (Data Processing Agreement)** — A contract between a data controller and data processor governing how personal data is handled, required under GDPR Article 28.

**DPO (Data Protection Officer)** — A named individual responsible for ensuring GDPR compliance within an organisation. Mandatory for certain organisations under GDPR Article 37.

**EU AI Act** — Regulation (EU) 2024/1689. The EU's primary AI regulation, classifying AI systems by risk level (Prohibited, High-Risk, Limited-Risk, Minimal Risk) and imposing corresponding obligations on providers and deployers.

**FMTI** — Foundation Model Transparency Index. A 100-indicator transparency framework developed by Stanford HAI, Berkeley, Princeton, and MIT for evaluating foundation model provider transparency.

**GDPR** — General Data Protection Regulation (Regulation 2016/679). EU data protection regulation governing the collection, processing, and storage of personal data of EU residents.

**GPAI (General-Purpose AI)** — AI models trained on large amounts of data that can perform a wide range of tasks. Subject to specific obligations under EU AI Act Articles 52–55.

**Industry profile** — A named configuration of dimension weights and critical criteria that contextualises an ATTA evaluation for a specific sector (healthcare, finance, etc.).

**ISO 27001** — International standard for Information Security Management Systems (ISMS), requiring systematic management of information security risks.

**ISO 42001** — International standard for AI Management Systems (AIMS), published December 2023 as the first ISO standard specifically addressing AI governance.

**LLM (Large Language Model)** — The AI model used in Stage 3 of the ATTA evaluation process to assess evidence and assign criterion scores.

**Model card** — A structured document accompanying an AI model that describes its intended use, performance characteristics, training data, known limitations, and evaluation results.

**N/A (Not Applicable)** — Designation for a criterion that genuinely does not apply to a vendor's scope (e.g., HIPAA for a non-healthcare vendor). Scored as 0 but not treated as a transparency failure.

**NIS2** — Network and Information Security Directive 2 (Directive 2022/2555). EU cybersecurity directive requiring security risk management and incident reporting for essential and important entities.

**PCI DSS** — Payment Card Industry Data Security Standard. Requirements for organisations processing payment card data.

**PHI (Protected Health Information)** — Individually identifiable health information regulated under HIPAA.

**Publicly discoverable evidence** — Information that a member of the public can access without contacting the vendor, signing an NDA, or creating an account. ATTA scores are bounded to this scope.

**Red-teaming** — A structured process where a team attempts to find failures, vulnerabilities, or harmful outputs in an AI system through adversarial testing.

**SOC 2 Type II** — An attestation report by an independent auditor evaluating a service organisation's controls over a defined period (typically 6–12 months) against AICPA Trust Service Criteria.

**SCC (Standard Contractual Clauses)** — Pre-approved contractual terms for GDPR-compliant transfer of personal data from the EU to third countries.

**VDP (Vulnerability Disclosure Policy)** — A published policy describing how security researchers can report vulnerabilities to an organisation and how the organisation will respond.

**Weighted score** — The overall ATTA score, calculated as the weighted sum of six dimension percentage scores using industry-profile-specific weights summing to 100%.

**ZDR (Zero Data Retention)** — An enterprise option where an AI vendor does not store customer inputs or outputs beyond what is required to process the immediate request.

---

*AI Transparency & Trustworthiness Assessment (ATTA) · Framework Documentation v3.1 · April 2026*

*This document is published for transparency purposes and may be reproduced or cited freely provided the source framework version and date are attributed. Vendors may link to or excerpt this documentation when explaining ATTA scores they have received.*
