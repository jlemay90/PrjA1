# PrjA1 Audit Plan

## Objective
Conduct a systematic, evidence-driven review of a target repository and produce reproducible findings, minimal fixes, validation evidence, and preventive recommendations.

## Evidence standard
Do not report a bug merely because code looks suspicious.

- **VERIFIED** — demonstrated by test, scanner, runtime behavior, advisory, or deterministic code path.
- **REPRODUCIBLE** — repeatable with documented steps.
- **PROBABLE** — strong evidence exists but a required verification step is blocked.
- **UNVERIFIED** — hypothesis requiring further evidence; never present as confirmed.

Prefer failing tests, reproducible behavior, scanner output, dependency advisories, logs, or demonstrable code paths.

## Workflow
1. **Map** — inventory structure, stack, dependencies, entry points, tests, docs, CI/CD, external services, trust boundaries, and critical paths.
2. **Discover** — inspect security, crashes/data corruption, functional defects, integrations, edge cases, dependencies/configuration, performance, and meaningful quality issues.
3. **Verify & Prioritize** — require evidence and record severity, impact, root cause, reproduction, complexity, and regression risk.
4. **Fix** — use the smallest safe change; add a failing regression test first when practical.
5. **Validate** — run relevant unit, integration, regression, static-analysis, security/dependency, build, and performance checks.
6. **Report** — maintain human-readable and machine-readable findings with coverage and uncertainty.
7. **Improve** — propose preventive tests, CI gates, monitoring, logging, architecture, and documentation improvements.

## Completion criterion
Systematically inspect all reachable repository areas and report coverage performed, tools used, areas not inspected, blockers, and remaining uncertainty. Continue until the audit checklist is exhausted or a documented blocker prevents further verification.

## Constraints
- Never compromise security for simplicity.
- Never fabricate findings, test results, scanner results, or coverage.
- Document assumptions explicitly.
- Respect API/service rate limits.
- Follow semantic versioning for intentional API changes.
- Prefer minimal, reversible fixes.
