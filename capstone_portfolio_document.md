# BBA Aviation Management – Capstone Project Document

**Course:** Generative AI for Business  
**Module:** Day 14 – Lab 14: Capstone GenAI Workflow Portfolio Presentation  
**Project Title:** End-to-End GenAI Workflow for Passenger-Complaint Management & Resolution  

---

## 1. Project Information & Team Details

* **Group Number:** Group 04  
* **Member 1:** [Student Name 1] (Roll No: [XXXXX01])  
* **Member 2:** [Student Name 2] (Roll No: [XXXXX02])  
* **Member 3:** [Student Name 3] (Roll No: [XXXXX03])  
* **Member 4:** [Student Name 4] (Roll No: [XXXXX04])  
* **Selected Project:** Option 2 — Passenger-Complaint Management  
* **GitHub Repository Owner:** [Student Name 1]  
* **Presentation Date:** September 25, 2026  

---

## 2. Business Brief

### Business-Brief Component Table

| Business-Brief Component | Student Response |
| :--- | :--- |
| **Project Title** | GenAI-Powered Passenger Complaint Management & Resolution Workflow |
| **Business Problem** | Slow response times to passenger complaints, generic non-helpful replies, and lack of actionable data for management to fix recurring service issues. |
| **Organisation / Context** | SkyHigh Airways (Customer Service & Quality Assurance Department) |
| **Target Audience** | Disgruntled passengers, frontline customer care staff, and senior airline management. |
| **Project Objective** | To build a fast, transparent workflow using GenAI to categorize, summarize, and draft personalized responses to passenger complaints while providing trend analysis for leadership. |
| **Required Outputs** | Complaint classification summary, auto-drafted customer response email, executive management report, and monthly complaint trend visuals. |
| **Verified Information Available** | Official airline refund/baggage policy, compensation terms, and flight log databases. |
| **Information Requiring Verification** | Specific compensation claims, actual delay reasons, and lost baggage tracking statuses. |
| **Privacy Considerations** | Removal of all personal data like full names, personal phone numbers, payment details, and booking references (PNRs) from public AI prompts. |
| **Compliance Considerations** | Adherence to DGCA passenger charter guidelines and airline customer compensation limits. |
| **Human Decision-Maker** | Customer Support Supervisor / QA Manager. |
| **Expected Final Deliverables** | Drafted customer response email, monthly complaint trend visual/infographic, management report template, and GitHub repository containing the prompt portfolio and audits. |

### Problem Statement
The selected aviation organisation, SkyHigh Airways, faces the problem of high volumes of unresolved passenger complaints causing delays, poor customer satisfaction, and high operational workload. The proposed workflow will use Generative AI to support complaint classification, text summarisation, customer email drafting, and management reporting. AI will assist with drafting and analysis, while authorised employees will remain responsible for verifying passenger claims, compensation amounts, and delay causes and approving the final outputs.

---

## 3. Workflow Mapping

| Stage | Input | AI Tool | Activity | Output | Human Responsibility |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | Raw complaint email from passenger | ChatGPT | Classify complaint type (e.g., lost baggage, delay, refund) and extract key facts. | Categorized summary sheet | Verify classification and ensure no PII was leaked. |
| **2** | Categorized summary + internal policy doc | Document-Grounded AI / Gemini | Draft personalized response following policy compensation rules. | Initial draft email | Check policy alignment and verify compensation calculations. |
| **3** | Monthly complaint dataset | ChatGPT / Claude | Analyze trends, group common issues, and write executive summary text. | Monthly trend report draft | Check logic, review metrics, and cross-reference operational logs. |
| **4** | Summary metrics & key points | Canva / Gamma | Convert structured data into a visual slide and infographic. | Visual dashboard & presentation slide | Review design for brand consistency and readable layout. |
| **5** | Drafted outputs & reports | None (Manual Gate) | Final human review gate using 4-dimension check (Accuracy, Tone, Compliance, Context). | Final approved deliverables | Sign off and hit send/publish. |

---

## 4. Tool Selection Matrix

| Business Requirement | Required Output | Selected Tool | Reason for Selection | Main Limitation |
| :--- | :--- | :--- | :--- | :--- |
| **Text Generation** | Complaint responses & report drafts | ChatGPT | High proficiency in tone matching, fast drafting, and structured output formatting. | Can hallucinate facts or policy rules if unguided. |
| **Current Information** | Recent aviation regulatory updates | Google Gemini | Integrated with real-time web search capabilities. | Outputs can sometimes be overly summary-focused without nuance. |
| **Image / Visuals** | Infographics for presentations | Canva / Gamma | Easy template integration and quick layout generation. | Struggles with precise, custom aviation icons without manual adjustment. |
| **Presentation Design** | Capstone presentation deck | Gamma / Canva | Automated slide layouts based on prompt text. | Auto-generated text on slides can be wordy and requires trimming. |
| **Document-Grounded Answers** | Policy verification checks | NotebookLM / Gemini | Grounded strictly in uploaded airline policy documents to avoid hallucination. | Dependent strictly on source document quality. |
| **Portfolio Storage** | File & project repository | GitHub | Industry-standard file hosting, version control, and markdown support. | Requires basic knowledge of markdown formatting and folder setup. |

---

## 5. Prompt Portfolio

### Prompt Record Matrix

| Prompt Version | Prompt | Problem Identified | Revision Made | Result |
| :--- | :--- | :--- | :--- | :--- |
| **Initial** | "Write an email apologizing to a passenger whose luggage was delayed for two days on flight SH102." | Too vague, lacked airline tone, made unapproved promises of cash compensation. | Added context, role, constraints, and explicit policy limits. | Response was better, but still missed refund details. |
| **Version 2** | "Act as a customer service representative for SkyHigh Airways. Write a professional email to [Passenger Name] apologizing for a 2-day baggage delay on flight SH102. State that we are looking into it." | Friendly tone, but lacked structure and instructions on baggage tracking steps. | Specified required output format, sections, and placeholder usage. | Clear structure, but tone felt slightly too mechanical. |
| **Version 3** | "Act as a SkyHigh Airways Customer Support Specialist. Draft a polite, empathetic email for a 2-day delayed baggage incident. Include: 1. Apology, 2. Tracking ID link placeholder, 3. Reference to policy section 4B for basic claim submission. Do not promise specific cash figures." | Accurate and professional, but needed a clear verification instruction for compensation. | Added explicit instruction to include a `[VERIFY]` tag for payout values. | Well-structured, safe, empathetic output. |
| **Final** | "You are a Customer Service Specialist at SkyHigh Airways. Write a concise, empathetic email to a passenger experiencing a 2-day baggage delay. **Constraints:** Use placeholders like `[Passenger Name]` and `[Baggage Claim #]`. Refer strictly to policy rules without promising exact compensation amounts. Tag any policy claims needing staff check with `[VERIFY]`. **Tone:** Professional, reassuring, direct." | None. Met all safety, tone, and formatting requirements. | Finalized for workflow deployment. | Workplace-ready, privacy-safe email draft. |

---

## 6. Workplace-Writing Output & Review

### Drafted Customer Response Email
> **Subject:** Update regarding your baggage – Flight SH102 / SkyHigh Airways  
>  
> Dear `[Passenger Name]`,  
>  
> Thank you for contacting SkyHigh Airways Customer Support. We sincerely apologize for the delay in receiving your checked baggage following flight SH102 from `[Origin]` to `[Destination]`. We understand how inconvenient this situation is and appreciate your patience.  
>  
> Your baggage tracking reference is `[Baggage Tag Number]`. Our ground team is currently processing the dispatch of your bag to your specified address.  
>  
> Under our passenger assistance policy, you may be eligible for reimbursement covering basic essential items purchased during this delay period. `[VERIFY: Check against Baggage Policy Section 4B for maximum daily allowance limit]`.  
>  
> To process an essential expenses claim, please submit your receipts through our online portal at `[Link]`.  
>  
> Warm regards,  
> **Customer Support Team**  
> *SkyHigh Airways*  

### Four-Dimension Review Gate

| Review Dimension | Question | Issue Identified | Correction |
| :--- | :--- | :--- | :--- |
| **Accuracy** | Is every factual claim supported? | The initial AI output promised a flat $200 cash payout immediately. | Replaced fixed dollar figure with policy link reference and a `[VERIFY]` tag. |
| **Tone** | Is the tone suitable for the audience? | First draft sounded defensive and transactional. | Revised prompt to demand an empathetic, apologetic, and clear structure. |
| **Compliance** | Are policies and commitments authorised? | AI claimed compensation applies within 2 hours of delay (Policy says 24 hours). | Updated text to reflect official 24-hour rule per regulation. |
| **Context** | Is the output suitable for its business use? | Output had fake contact details and passenger names filled in. | Swapped real-looking details for standard brackets (e.g., `[Passenger Name]`). |

---

## 7. Visual / Designed Output

* **Visual Objective:** Create a clear, executive-ready slide layout summarising quarterly passenger complaint trends for senior management.  
* **Target Audience:** SkyHigh Airways Quality Assurance Committee & Operations Leads.  
* **Initial Prompt:** "Make a colorful chart showing baggage and delay complaints for an airline."  
* **Problems Identified:** Too generic, bright distracting colors, inaccurate axis labeling, and clutter.  
* **Refined Prompt:** "Design a clean, professional corporate visual template showing a bar chart comparison of Q1 vs Q2 complaint types: Baggage Delays, Flight Delays, Refund Issues, and Staff Conduct. Tone: Clean, minimalist, corporate blue and gray palette."  
* **Final Visual Summary:** A visual dashboard layout highlighting that **Flight Delays (42%)** and **Baggage Delays (35%)** make up the majority of customer issues, complete with a clean callout box for action items.  
* **Ethical Consideration:** Ensuring scale ratios accurately represent data points without distorting percentages to make performance look better than it is.

---

## 8. Audits & Verification

### Hallucination Audit

| AI-Generated Claim | Evidence Available? | Supported, Partly Supported or Unsupported? | Action Taken |
| :--- | :--- | :--- | :--- |
| Passengers automatically receive $150 compensation for 2+ hour delays. | No | Unsupported | Removed dollar figure; replaced with reference to regulatory claim portal. |
| Baggage claim processing takes under 12 hours guaranteed. | No | Unsupported | Reworded to "typically processed within 24 to 48 hours." |
| DGCA guidelines mandate hot meals for any delay past 1 hour. | Yes | Partly Supported | Corrected time frame to match actual guidelines (typically 2+ hours depending on flight tier). |

### Privacy Audit

| Privacy Question | Yes/No | Action Taken |
| :--- | :--- | :--- |
| Were real personal details used? | **No** | Verified that no real customer names, phone numbers, or PNRs were entered. |
| Were placeholders used? | **Yes** | Replaced all real values with standard tags like `[Passenger Name]`, `[PNR]`. |
| Was data minimisation applied? | **Yes** | Stripped out all unnecessary customer information prior to prompt input. |
| Was confidential information excluded? | **Yes** | Excluded internal financial accounts and confidential system access codes. |
| Is the GitHub portfolio safe for public viewing? | **Yes** | Double-checked files; no secret keys, confidential data, or real credentials present. |

### Verification Trail

| Claim | Source | Does the Source Match? | Context Preserved? | Final Action |
| :--- | :--- | :--- | :--- | :--- |
| Mandatory compensation for baggage delay after 24 hrs. | Airline Passenger Service Charter | Yes | Yes | Retained in drafted policy summary. |
| Maximum daily allowance for essential expenses. | Internal Baggage Policy Document | Yes | Yes | Marked as `[VERIFY: Check current daily rate limit]`. |

### Severity × Risk Triage

| Problem Identified | Severity | Risk | Action Taken |
| :--- | :--- | :--- | :--- |
| AI hallucinated cash compensation amount in email. | High | High | Immediately removed payout quote; replaced with standard review process step. |
| Oversimplified complaint classification in dashboard. | Medium | Low | Updated categories to mirror operational taxonomy. |
| Missing source link for regulatory claim limits. | Low | Medium | Added direct citation to official charter document in footer. |

---

## 9. Final Presentation Overview (Slide-by-Slide Outline)

* **Slide 1: Title Slide** — Project Title, Group 04 Members, BBA Aviation Management, Course & Date.
* **Slide 2: Business Problem** — High passenger complaint volume leading to slow response times and lack of clear service trend insights.
* **Slide 3: Project Objective** — Implement an end-to-end GenAI workflow to categorize complaints, speed up response drafting, and produce management reports safely.
* **Slide 4: Tool Selection Rationale** — Summary breakdown of ChatGPT, Gemini, Canva/Gamma, NotebookLM, and GitHub roles and limits.
* **Slide 5: Proposed GenAI Workflow** — Diagram showing Input → GenAI Processing → Human Verification Gate → Final Business Deliverable.
* **Slide 6: Prompt Portfolio** — Comparison of Initial Prompt vs. Final Refined System Prompt highlighting iterative improvements.
* **Slide 7: Generated Outputs** — Side-by-side display of the customer response email and the quarterly complaint visual dashboard.
* **Slide 8: Review & Corrections** — Audit summary detailing how hallucinated compensation promises were identified and removed.
* **Slide 9: Verification Trail** — Breakdown of source citations, policy cross-checks, and `[VERIFY]` placeholder tags.
* **Slide 10: Risks & Human Review** — Highlight of privacy, bias, and accuracy risks, reinforcing the mandatory human-in-the-loop sign-off.
* **Slide 11: Recommendations & Conclusion** — Practical deployment steps for airline staff, emphasizing speed improvements while maintaining human oversight.
* **Slide 12: Reflection & GitHub Link** — Summary of learnings, key limitations observed, and direct link to the public GitHub repository.

---

## 10. Student Reflection & Answers

1. **Three Key Learnings:**
   * GenAI is an excellent assistant for drafting structure and content fast, but it cannot replace human review.
   * Detailed, constrained prompts produce vastly superior results compared to simple single-line requests.
   * Protecting data privacy requires active effort—placeholders are essential when working with customer communications.
2. **Application to Aviation Management:**  
   Aviation operates under strict safety, legal, and operational rules. GenAI can dramatically speed up routine communication and data summarisation, but every output must be aligned with actual aviation policies and regulatory frameworks before being published.
3. **Most Useful AI Tool:**  
   ChatGPT was the most versatile for text structuring and response drafting, while NotebookLM/Grounded Gemini was the most reliable for checking answers directly against uploaded policy documents without factual drift.
4. **Prompt Improvement:**  
   Initial prompts were far too brief and produced broad, generic text. Adding clear roles, specific constraints, required formats, and placeholder requirements made the outputs immediately usable for workplace scenarios.
5. **Incorrect Information Identified:**  
   The AI hallucinated a specific monetary refund guarantee ($150) that was not part of the standard policy and misstated delay time thresholds.
6. **Verification Method:**  
   Claims were verified by cross-referencing all generated text directly against official company policy PDFs and civil aviation regulatory charter guidelines.
7. **Privacy and Compliance Risks:**  
   Main risks included accidentally feeding real customer details (names, PNR numbers) into public AI models and committing the airline to unauthorized financial promises.
8. **Decisions Requiring Human Judgement:**  
   Final approval of passenger compensation payouts, exceptions to standard policies, emotional tone checks for severe complaints, and publishing public management reports.
9. **Improvements for Future Projects:**  
   Set up a dedicated policy vector database/custom GPT earlier in the process to reduce initial drafting hallucination rates even further.
10. **Career Support:**  
    This project demonstrates how to practicalize AI in corporate workflows safely, balancing modern productivity tools with legal compliance, privacy protection, and professional quality standards.

---

## 11. GitHub Repository Structure & AI Declaration

```text
day-14-capstone-portfolio/
│
├── README.md
├── business-brief.md
├── tool-selection.md
├── prompt-portfolio.md
├── workplace-writing-output.md
├── review-and-verification.md
├── reflection.md
├── presentation/
│   ├── final-capstone-presentation.pdf
│   └── final-capstone-presentation.pptx
├── visuals/
│   └── final-visual.png
└── sources/
    └── sources-and-links.md
```

### AI Usage Declaration
Generative AI tools (ChatGPT, Google Gemini, Gamma, Canva) were used to support drafting, summarisation, visual creation, and presentation development for this capstone project. All AI-generated outputs were rigorously reviewed by the project team for accuracy, tone, compliance, context, privacy, and source support. The team retains full responsibility for the final contents, analysis, and decisions presented in this work.