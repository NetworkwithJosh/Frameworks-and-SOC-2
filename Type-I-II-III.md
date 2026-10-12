A SOC 2 Type I examination addresses control design as of a specified date. A Type II examination also addresses operating effectiveness over a defined period. AICPA publishes illustrative Type II reporting materials under the applicable attestation requirements.

Before testing begins, the organization must define the system and report scope.

Scope may consider:
Services and commitments
Infrastructure
Software
People
Procedures
Data
Locations
Subservice organizations

Control mapping connects one control to multiple requirements or criteria when the control addresses the relevant objective.

Mapping does not mean every requirement is identical. The person performing the mapping must understand the intent of each requirement and document any gaps.

Map one access-review control to three possible security requirements or objectives.

Using the resources, recommend which systems, processes, and vendors belong in scope. Identify any initial management scope decisions that require clarification.

SOC 2 examination	What the examiner evaluates
Type I	Whether controls are suitably designed as of a specified date
Type II	Whether controls are suitably designed and operated effectively throughout a defined period

### 1. Access Review Control Mapping

**Selected Control:** Quarterly User and Privileged Access Reviews (POL-AC-002, Requirement 8).

Northstar requires quarterly reviews of user and privileged access to in-scope systems.

This control supports three security objectives:

1. **Least Privilege:** Ensures users maintain only the permissions necessary for their job responsibilities.
2. **Authorized Access:** Helps identify accounts with inappropriate or unnecessary access.
3. **Privileged Access Oversight:** Ensures administrator accounts and elevated permissions receive appropriate review.

Although this control supports multiple objectives, additional procedures and evidence may be necessary to satisfy different framework requirements.

### 2. Recommended SOC 2 Scope

**Systems**

I recommend including systems that process restricted customer information or support the security and operation of the CareBridge platform.

Key systems include:

- CareBridge Production and AWS Management Plane
- Okta for identity and access management
- Snowflake and CareBridge Analytics DB
- GitHub Enterprise and Jira Cloud
- Zendesk and Twilio
- Supporting monitoring, incident response, endpoint security, and compliance systems

Salesforce requires additional review because it contains customer information but is currently excluded from scope.

**Processes**

The assessment should cover access management, quarterly access reviews, employee offboarding, change management, incident response, vendor risk management, data protection, backup and recovery, and security awareness training.

**Vendors**

I recommend prioritizing AWS, Okta, Snowflake, Zendesk, and Twilio because of their roles in hosting, authentication, restricted-data processing, customer support, and notifications.

Other vendors supporting in-scope controls and operations should also be evaluated. Management should determine the appropriate treatment of relevant subservice organizations.

### 3. Management Scope Clarifications

Before finalizing scope, I would ask management to clarify the following:

- **Salesforce:** Why is it excluded despite storing customer contact information and implementation notes?
- **Snowflake:** What is the remediation plan for its overdue vendor risk review and outdated SOC 2 assurance report?
- **Twilio:** Why is it classified as Low risk despite processing patient contact information, and why is its recorded access review so old?
- **CareBridge Analytics DB:** Why are backups performed weekly when the policy requires daily backups for Tier 1 critical production data?
- **Okta:** Are the two service accounts excluded from MFA covered by approved exceptions and compensating controls?

These issues require additional investigation before determining whether the current scope and controls are appropriate.

### 4. Discussion: Risk of Incorrect Control Mapping

Assuming that a control mapped to one framework automatically satisfies another can create security and compliance gaps. Different frameworks may have different expectations regarding control objectives, implementation, frequency, and evidence.

Each requirement should be evaluated individually to determine whether the control adequately addresses it. Mapping identifies relationships between controls and requirements, but it does not prove that the controls are suitably designed or operating effectively.
