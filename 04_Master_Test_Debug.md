Act as a lead software engineer, reviewer and QA engineer. We are in T = TEST of the RPSBTCPD flow. Use actual assignment acceptance criteria and actual implementation, not assumptions.

ORIGINAL REQUIREMENTS:
[PASTE OR REFERENCE]
CURRENT FEATURE/FAILURE:
[INSERT]
ACTUAL ERROR/OUTPUT IF ANY:
[INSERT]

1. Inspect relevant code, tests, logs and build output where authorized.
2. Identify root causes, ordered by severity: Blocker, High, Medium, Low.
3. Recommend and apply the SMALLEST safe fix; don't rewrite unrelated working code.
4. Validate critical end-to-end flow, API status codes, input validation, calculations, null/empty cases, persistence and frontend-backend integration.
   When Clean Architecture is approved, inspect affected project/package dependencies and boundaries: Domain is independent of outer layers/frameworks; Application references Domain and defines necessary boundaries; Infrastructure implements them and owns persistence/provider integrations; API delegates use cases and uses Infrastructure only for composition. Flag concrete DbContext/provider leakage, circular references, and misplaced business/HTTP logic. Use existing architecture tests where available. Request approval for broad architectural refactors rather than treating them as routine bug fixes; do not impose Clean Architecture on an existing application without approval.
5. Check common security issues: hardcoded secrets, unsafe serialization/HTML, unauthorized resource access, untrusted AI context, unsafely executable tools and unbounded agent loops, only where applicable.
6. For RAG, verify retrieved-source accuracy, auth filters, empty-context abstention and mock-vs-real behavior.
7. Run relevant builds and tests; do not claim a pass unless commands were actually executed. Provide PASS/FAIL/NOT RUN evidence.
8. Compare implementation against all remaining P0 criteria. Prioritize missing P0 and crashes above minor polish.
9. Before Git commit, review diff, generated files, secret exposure and appropriate ignore rules.
10. Return recommended commit message and push verification commands, but do not commit/push automatically without approval.

RETURN:
- Root cause and issues in priority order
- Minimal fixes and files touched
- Actual test/build results, expected vs actual where relevant
- Open blockers and remaining P0
- Git commit/readiness checklist

Stop after current review; await my next instruction.
