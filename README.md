# kql-detection-library

> Detection rules for Microsoft Sentinel written in KQL, each mapped to MITRE ATT&CK, with the data needed to test it and notes on tuning false positives.

**Status:** Active. Rules are added as I write and test them in a lab workspace.

## Why

A detection rule is only useful if you can explain what it catches, prove it fires, and keep it quiet on normal activity. Every rule here ships with all three.

## Layout

```
detections/
  initial-access/
  credential-access/
  lateral-movement/
  persistence/
docs/
  rule-template.yaml    # copy this for every new rule
  testing.md            # how each rule is tested
```

## Rule index

| Rule | ATT&CK | Data source | Severity |
|---|---|---|---|
| _(first rule goes here)_ | | | |

## Principles

- Every rule maps to at least one ATT&CK technique ID
- Every rule has a test: sample events that should trigger it, and events that should not
- Every rule documents known false positives and how to tune them
- No customer or employer data: lab data and synthetic events only
