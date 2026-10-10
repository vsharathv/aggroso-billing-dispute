# Billing Dispute Investigation and Resolution Agent - Aggroso Expert Task

Live: http://localhost:8081

## AI Workflow
- Classify ambiguous description into OVERCHARGE/DUPLICATE/SERVICE_NOT_RENDERED/FEE_DISPUTE/CONTRACT_MISMATCH
- Retrieve relevant policy from knowledge base
- Explain why refund is eligible or not with evidence
- Cite policy section (Sec 4.2, Sec 3.1, Sec 5.4, Sec 6.1)
- Confidence percentage with uncertain flag if <90%
- Detect missing info and ask clarification

## Deterministic Validation
- Duplicate invoice ID detection
- Billed vs Contract amount difference calculation
- Missing document check (contract copy, receipt)
- Date validation
- Refund limit check as per policy

## Reviewer Actions
- Approve refund / Reject dispute
- Request clarification from customer
- Override AI classification with reason
- Complete decision history with timestamp

## Run
mvn spring-boot:run
Open http://localhost:8081
Login: investigator / admin
Vault Password: aggroso2024