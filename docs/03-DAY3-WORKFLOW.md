# ForgeSec – Rapid Security Risk Review Workflow (v1.0)

**Service Name**: Rapid Security Risk Review
**Agent**: ForgeSec
**Output**: Client-Ready Risk Report
**Pricing Tier**: Basic Audit

---

## 1. INPUT STANDARD
When a client provides information (email, chat, or document), format it into this block before sending it to ForgeSec:

> **CLIENT CONTEXT:**
> [Paste client description here]
>
> **SPECIFIC CONCERNS:**
> [Paste specific worries here, e.g., "We are worried about phishing"]
>
> **TECHNICAL DATA:**
> [Paste logs, config snippets, or policy text here]

---

## 2. AGENT INSTRUCTION (The "Money Prompt")
(Copy this prompt into ForgeSec to run the workflow)

You are performing a "Rapid Security Risk Review" for a client.
Based *only* on the provided context:

1.  **Calculate an Overall Risk Score:** (Low / Medium / High / Critical)
2.  **List Top 3 Priorities:** The three most urgent things to fix.
3.  **Generate the Full Report:** Use the standard "ForgeSec Security Assessment" format.

**CRITICAL INSTRUCTIONS:**
- If the risk is HIGH, the tone must be **urgent but supportive**.
- If the risk is LOW, the tone must be **validating**.
- Do NOT hallucinate data not in the context.
- Keep recommendations realistic for the client's size.

---

## 3. QUALITY CHECK (Human Review)
Before sending the report to the client, verify:
- [ ] Does it answer the client's specific concern?
- [ ] Are the recommendations actually possible for their size? (Don't suggest Enterprise tools for a 3-person shop).
- [ ] Is the "Overall Risk Score" accurate based on the findings?
