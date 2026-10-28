# DevCleaner Agent Guidance

## Authority and scope

GitHub Issues own the **current** task scope, acceptance criteria and dependency graph. `docs/DevCleaner-v1-requirements-review.md` retains approved product decisions and non-negotiable safety invariants; it is not another execution plan. Recheck `main`, upstream prerequisites and open PRs before acting. If a conflict remains, resolve the authoritative owning issue rather than inventing a parallel workflow.

Follow the currently installed shared Harness `AGENTS.md` and canonical `software-comments` and `software-architecture` policies (including One Word naming). Read their **actual accepted paths**; do not copy policy bodies, hard-code historical locations or invent substitute rules.

## Engineering

Prefer cohesive F# modules, pure functions, immutable typed domain decisions and explicit effects at I/O boundaries. Convert expected .NET/Windows failures to `Result` or async `Result`, preserve cancellation and real unexpected faults; avoid blanket exception swallowing and speculative plugin frameworks. Build the smallest working vertical slice first; retain existing build/security/CI gates and verify behavior manually before adding focused tests.

## Safety and delivery

Read and classification never authorize disposal. Respect exclusions, Git working trees, link/volume boundaries, mutation-time revalidation, quarantine/restore and explicit user approval for destructive or external changes. Never silently clear quarantine, discard real user data, expose secrets, or auto-retry ambiguous effects. Observe actual effects instead of trusting exit codes alone.

Use the canonical Workflow task lifecycle, project-specific GitHub issue and independent PR review. External writes, release publication and active runtime changes require their trusted approvals. No backward-compatibility layer or retained obsolete implementation solely for historical behavior.
