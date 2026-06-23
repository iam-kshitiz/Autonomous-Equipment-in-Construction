# Autonomous Construction Equipment — Per-Company Layer Classification

Scope: patents with priority date >= 2024 (as supplied), filtered to those that map to one of the 8 autonomy-stack layers AND carry an autonomy / automated-control / intelligent-sensing signal.

**Method:** automated keyword screening over title + abstract (strict autonomy gate). This is a screening pass for human review, not a verified legal classification. Full independent claims were not analysed.

| Company | Total (>=2024) | Kept (autonomy+layer) | L1 | L2 | L3 | L4 | L5 | L6 | L7 | L8 |
|---|---|---|---|---|---|---|---|---|---|---|
| Caterpillar | 604 | 35 | 16 | 3 | 1 | 0 | 2 | 11 | 1 | 1 |
| John Deere | 1153 | 37 | 13 | 1 | 10 | 10 | 3 | 0 | 0 | 0 |
| Komatsu | 557 | 41 | 5 | 1 | 2 | 11 | 0 | 1 | 1 | 20 |
| Volvo CE | 119 | 6 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 4 |
| XCMG | 2269 | 87 | 23 | 0 | 11 | 20 | 5 | 7 | 3 | 18 |
| Trimble | 55 | 7 | 5 | 0 | 0 | 2 | 0 | 0 | 0 | 0 |

Layer legend: L1 Perception, L2 Localisation, L3 Path Planning, L4 Grade Control, L5 Machine Interface, L6 Fleet Coordination, L7 Digital Jobsite Integration, L8 Remote Operations.

Counts above are by **primary** layer (each patent counted once). A patent may also map to secondary layers (see per-company CSVs).


## Note on Trimble (distinct profile)

Trimble's supplied file (55 patents) behaves very differently from the 5 OEMs, so it was reviewed in full:

- **Most of the portfolio is out of scope for "autonomous equipment."** It is dominated by **survey instruments** (total stations, surveying poles/rods, GNSS antennas, calibration) and **GNSS correction infrastructure** (ionospheric disturbance data) — positioning *technology*, not autonomous *machines*. These were correctly excluded.
- **A cluster of 12 "Autonomous vehicle" filings** (GB2025034xx) are assigned to **AGCO International / PTx Trimble** — Trimble's *agricultural* JV — and have empty abstracts. Excluded as agricultural autonomy (out of scope per the brief), not construction.
- **2 entries were added manually** (flagged `manual` in the CSV, Autonomy Signal = "manual"): `US2025277808A1` (implement-on-ground detection) and `EP4735697A1` (auto swing-boom control to an alignment). Both are **Caterpillar Trimble Control Technologies** construction-machine patents that the keyword pass missed only because their supplied abstracts are empty/too short. Layer assigned by human judgement.

Net Trimble = 7 (5 automated + 2 manual). The genuinely construction-relevant Trimble autonomy IP here centres on **perception/computer-vision** (site orchestration, perception-accuracy verification, LiDAR/point-cloud) and **grade control** for earthmoving implements.
