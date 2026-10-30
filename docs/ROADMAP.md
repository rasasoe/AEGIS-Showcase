# AEGIS — Development Roadmap

**Status: In Development** · Last evidence checkpoint: **2026-10-26**

This is a transparent engineering roadmap, not a product release schedule. A milestone is considered complete only when the relevant runtime or evidence confirms it.

## Verified so far

- Python controller, scope and approval infrastructure, and the PentAGI integration layer are implemented.
- Windows Ollama, local relay, and PentAGI returned an actual GPT-OSS 20B response.
- PentAGI's official mock tool-call compatibility checks passed **9/9**.
- The full automated regression suite passed **305/305** at the latest recorded checkpoint.
- A persistent lifecycle monitor was implemented and exercised with synthetic fault, cancellation, and restart scenarios.
- Worker status was **STOP** and target requests / newly created flows were **0** at that checkpoint.

## Next gates

| Gate | Evidence required | Status |
| --- | --- | --- |
| Native lifecycle safety | A limited no-target Flow stops through explicit STOP and timeout; native task/worker cleanup is observed | Pending |
| Admission/STOP reconciliation | Live state and independent guard agree; failures remain fail-closed | Pending native verification |
| First isolated laboratory run | Explicitly approved local lab, bounded execution, visible telemetry | Not started |
| First evidence-backed finding | Reproducible observation and manually reviewable HTTP evidence | Not demonstrated |
| Public technical demonstration | Sanitized captures, testing notes, clear limitations | Planned |
| Wider security-tutor integration | Documented learning and reporting workflow | In progress |

## Evaluation principles

- Do not label simulated behavior as native integration success.
- Do not claim a vulnerability is real without retained evidence.
- Do not publish credentials, internal service topology, or private code.
- Do not imply that a framework dependency is original AEGIS code.
- Do not run tests against third-party or unapproved targets.

## Planned updates

Once a milestone is verified, this repository will include a dated, sanitized experiment note with the environment assumptions, observed steps, outcomes, and limitations. Pending work stays marked **pending** until then.

[Back to project overview](../README.md)
