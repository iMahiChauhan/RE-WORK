# RE:WORK Interview Preparation

## 30-Second Explanation

RE:WORK is an AI-powered workforce recomposition engine. It helps employers identify whether a candidate has a genuine capability gap or is being filtered out by weak proxies such as degree brand, location, career breaks, or continuous tenure.

Instead of simply rejecting a candidate, it analyzes their evidence, decomposes the job into real tasks, identifies missing capabilities, recommends targeted learning and proof-of-skill activities, and gives HR an explainable recommendation for human review.

RE:WORK is a reasoning layer alongside SAP SuccessFactors, not an ATS, chatbot, autonomous hiring system, or ordinary job recommender.

## Business Problem

Traditional hiring systems often compare keywords, degrees, job titles, and years of experience. This creates false negatives for career returners, career switchers, rural or tier-2/3 talent, internal mobility candidates, and people with non-linear experience.

This matters because companies lose potentially capable talent, while candidates receive no actionable explanation or development path.

RE:WORK asks:

> What can this person actually do, what does the role require, what evidence is missing, and what is the smallest pathway to become viable?

## Main Workflow

`DISCOVER -> DECOMPOSE -> DIAGNOSE -> RECOMPOSE -> DEVELOP -> PROVE -> MATCH -> REVIEW`

1. Analyze candidate profiles and evidence.
2. Break a job into outcomes, tasks, capabilities, and requirements.
3. Separate genuine skill gaps from eligibility or workplace constraints.
4. Recommend targeted learning or work-design interventions.
5. Evaluate a proof-of-skill task using a rubric.
6. Recalculate opportunity readiness.
7. Generate explanations and audit information.
8. Keep the final decision with a human.

## Canonical Demo

The main demo follows Ananya, a career returner from Lucknow applying for a junior data analyst role.

The system identifies existing evidence of SQL and analytical capability, treats Power BI or dashboarding as a trainable gap, and treats career break, location, and continuous-tenure requirements as possible proxies rather than automatic skill gaps. It then produces a targeted learning pathway, proof-of-skill task, readiness assessment, and explainable HR recommendation.

## Contribution

Use this answer only where it accurately reflects your work:

> I contributed to the RE:WORK prototype across the backend, orchestration flow, SAP adapter boundary, explainability, and evaluation system. My main focus was connecting candidate evidence, job decomposition, diagnosis, learning, proof-of-skill, opportunity analysis, and human review into one auditable workflow.

Technical version:

> I worked with FastAPI, typed shared state, graph-based orchestration, deterministic services, fixture-backed SAP adapters, API routes, schema validation, audit events, and automated evaluation. I also helped ensure simulated data was clearly labeled and never presented as live SAP data.

Do not claim independent ownership of the entire repository unless that is accurate.

## Data Used

- Candidate profiles, resumes, projects, portfolios, and assessments
- Skills, proficiency, confidence, recency, and verification data
- Job outcomes, tasks, requirements, credentials, locations, and workplace conditions
- Learning resources, milestones, and completion criteria
- Proof-of-skill submissions, rubrics, scores, and evidence
- Opportunity readiness and employer workplace data
- Synthetic market signals
- SAP-shaped workforce, skills, learning, and opportunity data
- Human review decisions and audit events

### Data Provenance

- `LIVE`: only after verified SAP metadata and retrieval
- `SIMULATED`: fixture-backed SAP-shaped demo data
- `SYNTHETIC`: RE:WORK-generated fixture or benchmark data
- `USER_PROVIDED`: candidate or HR supplied evidence

For the current demo, SAP data is simulated, market data is synthetic, Ananya's proof is a demo fixture, and default persistence is in-memory.

## Technology Stack

### Backend

- Python, FastAPI, and Uvicorn
- Pydantic and pydantic-settings
- SQLAlchemy with PostgreSQL support
- LangGraph-style explicit orchestration
- HTTPX
- Pytest and pytest-asyncio
- Ruff

### Frontend and Infrastructure

- Next.js, React, TypeScript, and Tailwind CSS
- Docker Compose
- Render deployment configuration
- Adapter abstractions for SAP and LLM providers
- Deterministic fallback fixtures for demo mode

## Technical Architecture

The backend uses shared typed state containing candidate data, job data, evidence, capabilities, gaps, learning pathways, proof results, opportunity readiness, explanations, audit events, confidence, and errors.

The orchestration flow connects candidate intelligence, job decomposition, diagnosis, counterfactual analysis, pathway generation, proof evaluation, capability refresh, opportunity viability, intervention simulation, and human review.

The design is hybrid:

- AI-capable components extract and classify information.
- Deterministic services perform matching, scoring, validation, governance, and state transitions.
- Humans retain responsibility for consequential employment decisions.

## Insights Produced

- Evidence-backed capability profiles
- Genuine capability gaps and evidence gaps
- Possible eligibility proxies
- Workplace constraints
- Counterfactual explanations
- Targeted learning plans
- Proof-of-skill requirements
- Current and future opportunity readiness
- Intervention impact projections
- Explainable HR recommendations

The central insight is that a candidate can be unsuitable today but viable after a small, measurable intervention.

## Business Impact

RE:WORK is designed to:

- Reduce false negatives in hiring and internal mobility
- Make transferable skills more visible
- Connect learning investment to a specific role
- Use proof instead of relying only on credentials
- Improve HR decision traceability
- Support reskilling and internal mobility
- Reduce dependence on unexplained proxy filters

The defensible claim is that the prototype demonstrates these capabilities. It does not yet prove improvements in hiring time, retention, productivity, or demographic fairness in production.

## Evaluation Results

- 22 executable benchmark scenarios
- 22/22 benchmark scenarios passed
- Classification agreement: `1.0`
- Governance violations: `0`
- Seven negative scenarios
- Demo health check: `PASS`
- Golden replay: `EXPLANATION_READY`

Avoid quoting a backend test total unless it has been verified immediately before the interview because different project documents report different counts.

## Interview Answers

### What business problem did you solve?

> We addressed the problem that traditional hiring systems measure profile similarity rather than actual capability. This can exclude capable returners, career switchers, and non-traditional candidates. RE:WORK separates genuine skill gaps from weak proxies and gives the candidate a measurable pathway to become viable.

### Why does it matter?

> It matters because employers lose capable talent and candidates receive opaque rejection decisions. The system makes decisions more explainable and connects a hiring gap to targeted learning or proof instead of treating every mismatch as permanent.

### What data did you work with?

> I worked with candidate evidence, skills, job tasks, job requirements, learning resources, proof-of-skill results, opportunity data, SAP-shaped workforce data, synthetic market signals, and human review decisions.

### What tools did you use?

> I used Python, FastAPI, Pydantic, graph-based orchestration, SQLAlchemy, PostgreSQL support, Pytest, Next.js, React, TypeScript, Tailwind CSS, Docker, and adapter abstractions for SAP and LLM providers.

### What analysis did you perform?

> I compared candidate evidence against decomposed job requirements, classified gaps, separated skill gaps from eligibility proxies, generated an intervention pathway, evaluated proof-of-skill, reassessed readiness, and produced an explainable recommendation.

### What was the business impact?

> The demonstrated impact is better traceability, targeted development, improved visibility of transferable skills, and reduced dependence on unexplained proxy filters. Production impact such as improved hiring or retention has not yet been measured.

### How did you ensure responsible AI?

> We used provenance labels, schema validation, confidence escalation, evidence-linked explanations, human review, prohibited-attribute checks, audit events, negative cases, and tests against hallucination and prompt-injection behavior.

## Limitations

- SAP is simulated, not connected to a verified live tenant.
- Market intelligence is synthetic.
- Proof and intervention results are simulated projections.
- Default storage is in-memory.
- Production authentication and authorization are not complete.
- Confidence scores are heuristic, not calibrated probabilities.
- The system does not prove demographic fairness.
- The system does not guarantee employment.
- The system does not autonomously hire or reject candidates.
- Live SAP write-back is not production-proven.

## Best Closing Statement

> RE:WORK is a working and testable prototype demonstrating how AI, deterministic reasoning, evidence, learning, and human governance can work together to make workforce decisions more inclusive and explainable. Its strongest value is not automatic hiring; it is finding the smallest evidence-backed pathway that can make a candidate viable.