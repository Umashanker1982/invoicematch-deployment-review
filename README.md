# InvoiceMatch: Customer Deployment & Operational Readiness Review

**Assessment: Customer Deployment & Operational Readiness Review** · by **Umashanker**

A 3-page deployment review for deploying an AI-powered workflow automation system, **InvoiceMatch**, into a large enterprise customer's private infrastructure, with strict security controls, customer-owned operations after launch, and internal governance.

## The review document

- 📄 **[deployment_review.md](deployment_review.md)**: read it on GitHub (the diagram renders in the page)
- 📄 **[deployment_review.pdf](deployment_review.pdf)**: the same document as a 3-page PDF

**Verdict:** ready for pilot **with conditions** (security sign-off of the egress allow-list and gateway; ≥ 97% accuracy and 0 wrong auto-approvals on anonymized real invoices; both hypercare drills passed).

## Where each requirement is covered

| # | Requirement from the brief | Section |
|---|---|---|
| 1 | Deployment architecture | [1. Deployment architecture](deployment_review.md#1-deployment-architecture) (diagram + model choice) |
| 2 | Customer constraints | [2. Customer constraints](deployment_review.md#2-customer-constraints) |
| 3 | IAM strategy | [3. IAM strategy](deployment_review.md#3-iam-strategy-least-privilege-each-identity-gets-only-what-its-job-needs) |
| 4 | Secrets management | [4. Secrets management](deployment_review.md#4-secrets-management) |
| 5 | Operational readiness | [5. Operational readiness](deployment_review.md#5-operational-readiness) |
| 6 | Runbook design | [6. Runbook design](deployment_review.md#6-runbook-design) |
| 7 | Knowledge transfer plan | [7. Knowledge transfer plan](deployment_review.md#7-knowledge-transfer-plan-three-stages-each-with-an-exit-check) |
| 8 | Productization opportunity | [8. Productization opportunity](deployment_review.md#8-productization-opportunity) |
| 9 | Risk assessment | [9. Risk assessment](deployment_review.md#9-risk-assessment) |

## The system being reviewed

InvoiceMatch reads supplier invoices with Claude (through the course's SharedLLM gateway), checks them against purchase orders and contracts with ten written rules, and routes each one under the customer's approval limits. *AI reads; rules decide; people approve.*

- **Working product (live demo):** https://invoicematch.onrender.com
- **Source code, tests, and full engagement documents:** https://github.com/Umashanker1982/invoicematch

The review's claims (accuracy, cost, safety gates, IAM, runbook) are backed by that repository's code, tests, and measured benchmarks.

## Files

| File | What it is |
|---|---|
| [deployment_review.md](deployment_review.md) | The review document |
| [deployment_review.pdf](deployment_review.pdf) | PDF version (3 pages) |
| [docs/architecture.png](docs/architecture.png) | Deployment architecture diagram (image) |

> Silverbrook Financial is a fictional customer created for this exercise. All data is sample data; no real company data is used.
