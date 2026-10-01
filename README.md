# system-design-architect

## Scope

This repository is a decision-making body of knowledge for system design at MAANG level. It does not catalog technologies or list their features. Every piece of writing here exists to answer one question: **given a real problem, with real constraints, which architecture do you choose — and why?**

Anyone who reads an article in this repository should walk away able to make and defend an architectural decision, not just recite what a technology does.

### What this repository covers

| Directory | Scope |
|---|---|
| `01-storage/` | Storage engine decisions — relational vs NoSQL vs NewSQL, LSM vs B-Tree, indexing, partitioning, replication, isolation levels, when a database choice is wrong and what it costs. |
| `02-cache/` | Caching decisions — cache-aside vs write-through vs write-behind, invalidation, TTL strategy, stampedes, hot keys, consistency vs latency tradeoffs, when caching hurts. |
| `03-messaging/` | Asynchronous communication decisions — queues vs streams vs pub/sub, delivery guarantees, ordering, backpressure, dead letters, exactly-once myths, sync vs async boundaries. |
| `04-distributed/` | Distributed systems fundamentals as decisions — consensus, quorums, CAP/PACELC in practice, clocks and ordering, idempotency, leader election, split-brain, partial failure. |
| `05-components/` | Building-block decisions — load balancers, API gateways, rate limiters, ID generators, schedulers, search, CDNs: when each is needed, when it is overkill, and what breaks it. |
| `06-case-studies/` | Real-world architectures decomposed — why the system was built that way, what constraints forced the design, what the alternatives were, and where it fails. |
| `07-interview-designs/` | End-to-end designs under interview constraints — requirement scoping, capacity estimation, decision narration, tradeoff defense at MAANG interview depth. |
| `08-production-analysis/` | Post-mortems and production behavior — outage analysis, bottleneck forensics, degradation patterns, what the architecture predicted vs what actually happened. |
| `09-projects/` | Hands-on implementations that prove or break the decisions documented elsewhere — build it, load it, fail it, measure it. |
| `10-cheat-sheets/` | Compressed decision references — numbers every architect should know, decision matrices, back-of-envelope formulas, comparison tables driven by tradeoffs, not features. |

### The contract every article must honor

Every article answers all nine, in order. An article that skips one is out of scope.

1. **Problem** — the real constraint being solved; scale, latency, consistency, or cost pressure that makes this a decision at all.
2. **Options** — the viable alternatives, stated fairly, including "do nothing" and "the boring choice."
3. **Decision** — which option wins under which conditions, and the reasoning that gets you there.
4. **Tradeoffs** — what you gave up by deciding; the cost of the choice stated as plainly as the benefit.
5. **Failure Modes** — how this decision breaks in production: overload, partition, corruption, cascading failure, human error.
6. **Metrics** — the numbers that tell you the decision is working or failing; what to measure, alert on, and capacity-plan against.
7. **Scaling** — how the decision behaves at 10x and 100x; where it holds, where it bends, where it must be replaced.
8. **Cost** — infrastructure, operational, and complexity cost; what this decision costs to run and to staff.
9. **Production Examples** — named real-world systems that made this choice, and what happened to them.

### Out of scope

- Feature lists, tool tutorials, installation guides, or vendor documentation rewrites.
- Technology descriptions with no decision attached.
- Comparisons that end in "it depends" without stating what it depends on.
