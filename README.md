FraudLens is ready — a fully self-contained, browser-only fraud detection engine. Here's what it runs against every file you upload:
**9 Detection Algorithms:**

1. **Benford's Law — Chi-square test + Mean Absolute Deviation** against the natural first-digit distribution. Fabricated data almost always fails this.
2. **Statistical Outliers — Z-score (3σ) + IQR (3×) methods combined** Flags both high-value extremes and contextual anomalies.
3. **Round Number Bias** — Natural transactions rarely end in .00 or 000. >30% is suspicious; >60% is flagged High.
4. **Threshold Proximity (Structuring)** — Catches amounts landing just below $500 / $1K / $2.5K / $5K / $10K approval limits — classic smurfing/structuring patterns.
5. **Duplicate Detection** — Exact row duplicates + near-duplicates (same vendor, same amount, within 7 days).
6. **Temporal Patterns** — Weekend/holiday transaction ratios, end-of-month clustering, velocity spikes (day-level Z-score).
7. **Sequence Gap Analysis** — Finds missing invoice/ID numbers that might indicate deleted records.
8. **Vendor Concentration** — Top-vendor spend share analysis for kickback/preferred-vendor fraud.
9. **TensorFlow.js Autoencoder** — An 8-feature neural network (amount, day-of-week, day-of-month, month, weekend flag, round flags) trained live on your data. Transactions it can't reconstruct are flagged as multi-dimensional anomalies.

**Everything runs in your browser** — no server, no API, no data leaves your machine.

Toggle switch with sun ☀️ / moon 🌙 icons and a sliding pill — orange accent knob that animates smoothly between positions.
Light mode — white cards, sky-blue backgrounds, deep navy text (your previous design).
Dark mode — near-black backgrounds, muted blue-grey text (the original dark design).
Both themes preserved fully — every color, border, badge, severity label, and hover state adapts via CSS variables with no hardcoded values remaining.
Chart axes update in real time when you toggle — grid lines and tick colors shift to match the new theme.
Preference is saved to localStorage so your choice persists across sessions.
