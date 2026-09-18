# Cyber Incident Response Plan

A structured Incident Response Plan (IRP) built for **Task 5** of the Internee.pk Cybersecurity Internship. Defines procedures for threat detection, mitigation, and recovery, grounded in a real, documented ransomware threat rather than generic theory.

## Overview

This plan follows the **NIST 6-phase Incident Response framework**:

| Phase | Purpose |
|---|---|
| 1. Preparation | Tools, policies, and training in place before an incident happens |
| 2. Detection & Analysis | Noticing something's wrong and confirming it's a real incident |
| 3. Containment | Stopping the attack from spreading further |
| 4. Eradication | Removing the actual threat from the environment |
| 5. Recovery | Restoring systems safely and confirming they're clean |
| 6. Lessons Learned | Documenting the incident to improve for next time |

## Threat Case Study: Conti Ransomware

Rather than a purely theoretical plan, this IRP is grounded in **Conti** — a real, documented Ransomware-as-a-Service tracked by the MITRE ATT&CK Framework as **Software ID S0575**, operated by the group **Wizard Spider**. Conti was used in the 2021 attack on Ireland's Health Service Executive (HSE), which shut down an entire national healthcare IT network.

Key MITRE ATT&CK techniques referenced in this plan:

| ATT&CK ID | Technique |
|---|---|
| T1059.003 | Command and Scripting Interpreter (Windows Command Shell) |
| T1083 / T1135 / T1057 / T1018 | Discovery (File, Network Share, Process, Remote System) |
| T1021.002 / T1080 | Remote Services (SMB) / Taint Shared Content |
| T1027 / T1140 | Obfuscated Files / Deobfuscate-Decode Files |
| T1489 | Service Stop |
| T1490 | Inhibit System Recovery |
| T1486 | Data Encrypted for Impact |

Source: [MITRE ATT&CK — Conti, Software S0575](https://attack.mitre.org/software/S0575/)

## Simulated Incident: "Operation Frozen Ledger"

A realistic, fictional ransomware incident timeline built entirely from Conti's documented techniques — from an initial phishing email through network discovery, lateral movement, defense evasion, and encryption. Notably includes a **dwell time of over a full day** between initial access and the destructive encryption event, highlighting why fast detection matters as much as prevention.

Full timeline and technique mapping: see [`IncidentResponsePlan.md`](./IncidentResponsePlan.md).

## What's Included

| File | Description |
|---|---|
| [`IncidentResponsePlan.md`](./IncidentResponsePlan.md) | Full plan in Markdown — objective, framework, case study, simulated attack timeline, response procedures, staff training guide |
| `Task5_Incident_Response_Plan.docx` | Formatted Word version of the plan |
| `Task5_Slides.pptx` | Slide deck summarizing the framework, case study, and procedures |

## Video Walkthrough

[Add your video link here once uploaded]

## Key Takeaway

Detection speed matters as much as prevention. The simulated timeline shows an attacker with over a day of undetected access before any destructive action — the kind of gap a well-tuned Detection & Analysis phase is specifically designed to close.

## Author

Soban Raja — Cybersecurity Intern, Internee.pk
