# RUN_LOG.md

---

## Setup Exercise — Your Search's Personal Layer
**Date:** 2026-06-25
**Operator:** Neha Dharanu

---

### What Was Built
Three files created in `search/` folder of forked Reallocation Engine repo:
- `search/resume.json` — structured, attested record extracted from resume PDF
- `search/profile.yml` — target role, visa constraints, geography, sponsorship gate
- `search/gaps.md` — delta between attested resume and SOC 15-1252 target role requirements

---

### Three Attestation Errors Caught in resume.json

1. **Kubernetes scope overclaimed** — agent listed Kubernetes as a peer skill alongside Docker and AWS, implying cluster ownership. Reality: used a managed Kubernetes cluster at Mercedes-Benz for dev/staging deployments — did not author cluster configs or Helm charts. Corrected by removing Kubernetes from the skills list and adding a `kubernetes_note` field with accurate scope.

2. **Hibernate/JPA omitted from skills** — agent extracted skills only from the skills section of the resume and missed Hibernate/JPA, which was used hands-on at Mercedes-Benz for query updates during the DB2-to-PostgreSQL migration. Corrected by adding Hibernate/JPA to the frameworks skills list.

3. **Capgemini contribution scope overstated** — agent wrote "owning design through production deployment" implying solo ownership. Reality: team of 4–6 engineers. Corrected bullet to "contributed... as part of a team of 4–6 engineers, participating from design through production deployment."

---

### Top Gap from gaps.md

**System design interview fluency** — I have real design work (Mercedes rules engine processing millions of automotive config rules, zero-downtime DB2→PostgreSQL migration, SentinelPay three-layer fraud detection architecture) but have not practiced articulating these designs under timed interview conditions at a target company. Gap closes when three written design docs are published on GitHub and reviewed by a practicing senior engineer, or a system design screen is passed at a target company.

---

### Killed Row and Why

**Killed:** Organizational leadership — mentoring junior engineers and driving alignment across teams

**Reason:** Agent generated this gap because mentoring activity does not appear explicitly in my resume. In reality, I informally mentored 1–2 junior engineers at Mercedes-Benz on task-level design and code reviews. The agent could not know this from the resume text alone — this is exactly the kind of domain knowledge about my own situation that required my correction. The gap is overstated; what I lack is formal team leadership, not all organizational influence.

---

### Field Corrected in profile.yml from Agent's First Draft

Agent wrote three fields incorrectly in its first draft:
- `hard_exclusions` — agent added Defense and Gambling as exclusions; I have no hard industry exclusions. Removed.
- `company_size` — agent excluded Series A entirely; I would consider Series A if H-1B sponsorship history is documented. Corrected.
- `work_arrangement` — agent wrote "not fully remote only" implying a geographic constraint. Reality: I am open to fully remote, hybrid, or in-office anywhere in the USA. Corrected.

---

### Verification Check Answers

**resume.json:** Every job entry is defensible. "Zero downtime migration" and "70% performance improvement" at Mercedes-Benz are both figures I measured and owned directly — confirmed yes.

**profile.yml:** Visa section reflects actual documents. OPT start date of October 2026 is based on expected EAD timeline confirmed with DSO. STEM OPT eligibility confirmed with DSO — marked as confirmed, not uncertain.

**gaps.md:** Censys job posting (8245190002) cited in evidence column is no longer live as of 2026-06-25 — verified by checking job-boards.greenhouse.io/censys which returned an error for that specific role. However, the Censys board shows active "Distributed Systems Engineer" and "Senior Backend Engineer" roles confirming the demand pattern is real and not invented. O*NET 15-1252 verified live at onetonline.org/link/summary/15-1252.00 and confirms distributed systems and design requirements for the occupation. One evidence citation is stale; the demand signal still holds.

---

*No contents from search/private-notes.md are included in this log.*
