# Suspicious PowerShell Detection

## Objective

Detect potentially suspicious PowerShell execution that may indicate malicious activity.

## Why This Detection Matters

PowerShell is a legitimate Windows administration tool, but attackers may also use it for execution, persistence, reconnaissance and other post-compromise activities.

## Detection Approach

This detection will focus on identifying PowerShell execution patterns that may warrant investigation.

## Data Sources

- Windows Event Logs
- PowerShell logging
- Sysmon
- EDR telemetry

## MITRE ATT&CK

- T1059.001 — PowerShell

## Investigation

When this detection triggers, the analyst should investigate:

- Which user executed PowerShell?
- Which host was involved?
- What command or script was executed?
- What process launched PowerShell?
- Was encoded or obfuscated content used?
- What happened before and after the PowerShell execution?
- Are there signs of persistence, credential access or lateral movement?

## False Positives

Legitimate administrative scripts and IT automation may generate similar activity.

## Future Improvements

- Develop detection logic
- Test against benign and malicious activity
- Identify false positives
- Tune the detection
- Map detection logic to relevant telemetry
