## Jedidiah Asaf Tallulembang

Forecasting, operations research and supply chain analytics. Currently at **Schneider Electric
Global Supply Chain**, owning forecast-accuracy measurement across nine countries. Completing an
**MITB (Data Science & Analytics)** at Singapore Management University.

I build the models *and* the tools that put them in front of the people who act on them.

---

### Selected work

**[ask-the-forecast](https://github.com/jediasaf/ask-the-forecast)** — an LLM planning agent that
answers questions about forecast performance by calling tools over real data, never by recalling or
computing numbers. Strict tool schemas, structured output with an explicit refusal path, and an eval
harness that checks mechanically that every cited figure came from an actual tool return.

Measured against a prompt-stuffing baseline across three question sets. On easy questions both reach
37/37 — stuffing the data into a cached prompt works fine, at 2.2× the cost. On questions needing
computation over the daily series the architectures separate: **agent 14/14, prompt-stuffing 6/14**,
because a baseline correctly forbidden from doing arithmetic can only refuse. Tools turned half that
set from unanswerable into answered.

**[forecasting-portfolio](https://github.com/jediasaf/forecasting-portfolio)** — four dashboards on
public data, each reporting its own failure modes.
[**Live →**](https://jediasaf.vercel.app)

- *Forecast backtest* — walk-forward on Walmart M5. Prophet 20.52% WAPE. The page also explains why
  the Elastic Net's 5.46% is **not** a fair comparison, and why `HOBBIES_2` fails at 34% on
  intermittent demand.
- *Forecast value add* — measured against a seasonal-naive baseline, the model adds **−5.7pp**.
  It loses on 5 of 7 departments and only earns its place on the hardest series.
- *Operations* — 240k flight movements. 45.8% of seats flew empty; ten points of utilisation
  separate the best and worst terminal.
- *F&B trading* — 735 trading days, fully indexed. Includes why the till's headcount field was
  rejected in favour of bill count.

**[ev-charging-site-optimisation](https://github.com/jediasaf/ev-charging-site-optimisation)** —
choosing EV charger sites in Singapore as a binary mixed-integer program (PuLP/CBC), trading coverage
gap against spatial spread. The max-min distance term is linearised with big-M constraints; the
objective weighting is swept to confirm the selection is driven by geography rather than tuning.

**[Vast-Challenge-2026](https://github.com/jediasaf/Vast-Challenge-2026)** — BreachLens. Visual
analytics reconstruction of an information-embargo breach across 912 messages and 77 public posts.
Quarto site with an interactive Shiny explorer.

---

### Working with

`Python` `SQL` `JavaScript / TypeScript` `React` `R`
`PuLP / CBC` `scikit-learn` `Prophet` `pandas`
`Tableau` `Power BI` `Grafana` `AWS` `SAP` `Kinaxis`

---

### A note on the numbers

Every figure in these repos is computed from stored outputs at build time, not restated from a
report. Where a model underperforms a naive baseline, or a metric turns out to be unusable, that is
on the page too — it is usually the more useful finding.

📍 Singapore · [LinkedIn](https://linkedin.com/in/jedidiahasaf) · jediasaf@gmail.com
