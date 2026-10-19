# Lab 02 – Microsoft Entra Sign-in Troubleshooting

**Environment:** Simulated Microsoft Entra ID  
**Role:** IT Support Technician  
**Ticket:** INC-002  
**Priority:** Medium

## Scenario

Sarah Collins, an employee in the Sales Department, reports that she cannot sign in to Microsoft 365.

She was able to access her account yesterday, but this morning her sign-in attempts are failing.

The Service Desk has received a ticket requesting an investigation into the authentication issue.

## Objective

Investigate the Microsoft Entra ID sign-in failure, identify the most likely cause, and recommend an appropriate resolution.

## Requirements

1. Locate the affected user account and verify its status.
2. Review the available sign-in logs and identify any errors.
3. Investigate the relevant authentication details.
4. Determine the most likely cause of the sign-in failure.
5. Recommend corrective actions without unnecessarily weakening account security.
6. Explain how to verify that access has been restored.
7. Document the investigation, evidence, findings and outcome.

## Investigation & Actions Taken

1. Located Sarah Collins' account in Microsoft Entra ID and confirmed that it was enabled.
2. Verified that the user had an assigned Microsoft 365 licence.
3. Reviewed the simulated sign-in logs and identified four failed authentication attempts on 19 October 2026.
4. Investigated error code **AADSTS50076**, which indicated that multifactor authentication was required.
5. Confirmed that password authentication had succeeded, indicating that an incorrect password was not the cause of the failure.
6. Contacted the user and discovered that she had replaced her phone and no longer had access to the previously registered Microsoft Authenticator.
7. Verified the user's identity according to company procedures.
8. Created a simulated **Temporary Access Pass (TAP)** with a 60-minute validity period and one-time use enabled.
9. Used the TAP recovery workflow to register Microsoft Authenticator on the new device.
10. Verified that the user successfully completed MFA and accessed Microsoft 365 services.

## Evidence

The following evidence was provided in the simulated training environment:

- **Evidence 01 – User Account:** Account enabled and Microsoft 365 licence assigned.
- **Evidence 02 – Sign-in Logs:** Four failed sign-in attempts, with the latest at 08:36 on 19 October 2026.
- **Evidence 03 – Authentication Error:** AADSTS50076, with successful password authentication and an MFA requirement.
- **Evidence 04 – Authentication Methods:** Old Microsoft Authenticator method unavailable and no alternative MFA methods registered.
- **Evidence 05 – TAP Configuration:** 60-minute validity and one-time use enabled.
- **Evidence 06 – Recovery Verification:** New Microsoft Authenticator registered, MFA test successful, and Outlook and Teams access restored.

*All evidence consists of simulated training data. No live Microsoft Entra tenant was modified.*

## Findings & Resolution

**Root Cause:** The user had replaced her mobile phone and lost access to the registered Microsoft Authenticator method. Her password was valid, but she could not complete the required MFA challenge.

**Resolution:** After identity verification, a one-time Temporary Access Pass was issued with a 60-minute validity period. The user successfully registered Microsoft Authenticator on her new phone and completed MFA.

The user confirmed successful access to Outlook and Microsoft Teams.

**Security Follow-up:** Review and remove the obsolete authentication method associated with the old device, according to company policy. This step was recommended but not executed in the simulation.

**Ticket Status:** Resolved – Ready for closure following security follow-up.

## Skills Practised

- Microsoft Entra ID user investigation
- Sign-in log analysis
- Authentication error identification
- MFA troubleshooting
- Temporary Access Pass recovery
- Secure identity verification
- Microsoft 365 access verification
- IT Support ticket documentation
