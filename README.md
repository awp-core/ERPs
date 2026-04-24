# Emission Reallocation Proposals (ERPs)

ERPs are periodic governance proposals that adjust the AWP emission weight vector across active WorkNets. Each ERP proposes a new allocation, supported by a standardized evaluation of the participating WorkNets.

All ERPs live in the [`ERPs/`](./) directory. The auto-generated public index is at [awp.pro/erp](https://awp.pro/erp).

## Process

1. Fork this repository.
2. Copy an existing ERP (e.g. [`ERP-0001.md`](./ERP-0001.md) / [`ERP-0002.md`](./ERP-0002.md)) as your template — the schema is stable across cycles.
3. Fill in:
   - Proposal metadata (ID, author, cycle, effective period)
   - Weight vector (current and proposed, per active WorkNet)
   - Evaluation framework scoring (per ERP-001 §4: four factors, 1–10 scale, weighted)
   - Impact analysis (per-WorkNet deltas, risks, mitigations)
   - Execution section (action list, contract call targets)
4. Open a PR against `main` with your ERP file.

## Statuses

| Status | Meaning |
|---|---|
| `Draft` | Author is drafting; not ready for review |
| `Review` | Open for community review and feedback |
| `Accepted` | Community consensus reached; eligible for on-chain execution |
| `Rejected` | Closed without adoption |
| `Final` | Applied on-chain; superseded by a later ERP when its effective period ends |
| `Superseded` | A later Final ERP has replaced this one |

State transitions are tracked via PRs that update the `status` field in the proposal frontmatter.

## Naming

- File name: `ERP-NNNN.md` (four-digit sequence, zero-padded).
- The next available number is `max(existing) + 1`.

## Related

- [AIPs](https://github.com/awp-core/AIPs) — broader Agent Improvement Proposals (WorkNet launches, protocol changes).
- [AWP Whitepaper §Governance](https://awp.pro/whitepaper#governance) — long-form context on the emission model.
- [awp.pro/dao](https://awp.pro/dao) — DAO interface where on-chain proposals are submitted once an ERP reaches Accepted.

## Questions

Join the discussion at [github.com/awp-core/ERPs/discussions](https://github.com/awp-core/ERPs/discussions).
