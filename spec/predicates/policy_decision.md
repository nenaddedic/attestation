# Predicate type: PolicyDecision v1

Type URI: https://in-toto.io/PolicyDecision/v1

## Purpose

Represents a policy decision (verdict) about an artifact or a set of artifacts.

## Schema

```jsonc
{
  "subject": [{ ... }],
  "predicateType": "https://in-toto.io/PolicyDecision/v1",
  "predicate": {                           // required
    "verdict": {                           // required
      "pass": "<BOOLEAN>"                  // required
      "message": "<STRING>"                // optional
    },
    "policy": {                            // required
      "id": "<URI>"                        // ?
      "digest": { /* DigestSet */ }        // ?
      "description": "<STRING>"
    }
    "metadata": {                          // optional
      "evaluatedOn": "<TIMESTAMP>",        // optional
    },
  }
}
```
