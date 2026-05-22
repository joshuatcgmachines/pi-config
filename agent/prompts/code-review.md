---
description: Review staged git changes
---

Review staged changes (`git diff --cached`) as a senior engineer.

- Focus on substantive issues only: bugs, regressions, reliability/performance risks, and missing tests.
- Ignore style-only nits.
- Max 5 findings, ordered by severity, each with file/line and one-line fix guidance.
- For each finding include: `Severity` (`critical|high|medium`), `Impact` (what can break), `Evidence` (file:line), and `Fix` (smallest safe change).
- Prefer high-confidence findings; avoid speculative comments unless clearly labeled with what evidence is missing.
- Explicitly check for: security/privacy risks, data-loss or migration hazards, API/contract breakage, and missing error handling/observability.
- Call out missing or weak test coverage with concrete test cases to add (happy path + one edge/failure path).
- If the change affects performance-sensitive paths, note likely hotspots and suggest a lightweight validation method.
- End with a short `Residual risks` section even when findings are present.
- If no significant issues exist, say so in one short sentence and list residual risks.
- Do not edit or commit.
