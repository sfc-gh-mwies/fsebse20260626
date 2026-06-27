# For the SE, By the SE — June 26, 2026
## Team Canada (Team Anand)

> *"No marketing replay. No exec decks. Just SEs sharing what's working — for SEs who need to go close deals."*

---

## Session Recording

**Recording:** [Zoom Link](https://snowflake.zoom.us/rec/share/IX3CBZYe38GKt-2PlNf9D17T5b3IiuWKHmtAGiKnVrqYQGsI7J5hm9rHr-rVTjw-.sYNgJ9we0B_d9I61)
**Passcode:** `#Du6GKG4`

**Slides:** [Google Slides](https://docs.google.com/presentation/d/10L6URO-kuN1aP9uVmqhQMRedP1UgQ9A3atV5Q5KOh1g/edit?usp=sharing)

---

## Agenda

| # | Topic | Presenter |
|---|---|---|
| 1 | Can We Really Be the Control Plane? | Mike Wies |
| 2 | Behind the Keynote: The Sanofi Story | Ken Reycraft |
| 3 | ClickHouse Compete: Interactive Analytics | Will Xu |
| 4 | Is Co-Work the New BI? | Sébastien Notebaert |
| 5 | Ontologies + Sense + Horizon Context | Vikram + Olivier |

---

## Resources

### ClickHouse Compete: Interactive Analytics
**Presenter:** Will Xu (Honorary Canadian)

- 9x higher QPS vs. Gen 1 at 200-concurrent-user load
- 3x lower latency at 0.6 CR/HR on XS
- 40% lower cost than Gen 1 warehouse at equal size
- $2.4/HR (Snowflake Interactive) vs. $3.6/HR (ClickHouse) on comparable hardware

**Demo**
- YouTube Demo: *(coming soon — placeholder for Will's ClickHouse vs. Snowflake benchmark video)*

**Blog Post**
- [Efficient Ingest for Query-Ready Data in Snowflake](https://www.snowflake.com/en/blog/engineering/efficient-snowflake-ingestion-query-ready/) — Will's official response to ClickHouse's cost benchmark. Covers the anti-patterns in their methodology (wrong warehouse gen, mixed ingestion architectures, excluded client-side costs), Snowflake's recommended production ingestion setup, and the Interactive Warehouse advantage for high-concurrency serving workloads.

---

### Ontologies Vs. Semantic Views
**Presenters:** Vikram + Olivier

When do semantic views reach their limits? A practical, customer-grounded look at ontologies on Snowflake

**The Core Framework**
| Question Type | Semantic View | Ontology / KG |
|---|---|---|
| Aggregations, filters, metrics | ✅ Native | Overkill |
| Fixed-depth joins (2-3 tables) | ✅ Native | Not needed |
| Variable-depth traversal | ❌ Limited | ✅ Core strength |
| Entity resolution / inference | ❌ Cannot | ✅ Native |
| "Why" reasoning chains | ❌ Cannot | ✅ Native |

> Best practice: **Semantic views for WHAT/HOW MUCH — Ontology for HOW/WHY/WHO-CONNECTS-TO-WHOM**

- [Ontology on Snowflake — GitHub](https://github.com/snowflake-Labs/ontology-on-snowflake)

---

*Hosted by Mike Wies | Team Canada (Team Anand) | June 26, 2026*
