# Booster Rocket Trade Study Analysis

## Overview
This project compares six booster rocket propulsion concepts: two liquid engines, two solid rocket motors, and two hybrid engines under a common mission requirement set. The goal is to select a concept to move forward with based on performance and practicality.

## Mission Constraints
- Ideal velocity change (ΔV): 2300 m/s
- Max burn time: 100 s
- Payload: 100,000 kg
- Vehicle diameter: 3 m

## Designs Compared
### Liquid Rocket Engines
1. LOX / RP-1
2. LOX / LH2

### Solid Rocket Motors
3. Aluminum / Ammonium Perchlorate (AP) with HTPB binder
4. Magnesium / Ammonium Nitrate (AN) with HTPB binder

### Hybrid Rocket Engines
5. HTPB fuel / LOX oxidizer
6. N2O oxidizer / Paraffin fuel

## Analysis Approach
### Performance + Thermochemistry (NASA CEA)
Key propulsion properties were generated using NASA CEA, including:
- Specific impulse (Isp)
- Characteristic velocity (c*)
- Specific heat ratio (γ)
- Optimal oxidizer/fuel ratio (O/F)
- Thrust coefficient (Cf)

Common CEA assumptions were used for consistency, including:
- Optimal expansion at sea level
- Initial chamber pressure: 1000 psia
- O/F sweep in 0.1 increments
- Frozen chemistry (NFZ 2 scenario)

### Sizing + Trajectory (Python / Jupyter Notebook)
For each design, the analysis computed:
- Average sea-level Isp
- Required motor sizing + nozzle sizing
- Propellant mass breakdown
- Propellant tank sizing
- Burn trajectory plots (altitude, velocity, acceleration vs time)

All mathematical analysis was completed in Jupyter Notebook.

## Key Outcome / Recommendation
The final selection depends on the priority:

- If simplicity and schedule dominate: a solid rocket motor (AP/Al) is recommended.
- If maximum performance is the goal: the LOX/LH2 liquid engine is recommended.

The report’s overall recommendation is LOX/LH2, due to substantially higher performance (nearly 100 seconds higher Isp, >30% improvement vs the second-best design) and comparatively clean exhaust products for the propellant pair in the quantities considered.

## Files
- `Booster_Rocket_Analysis.pdf` — Full report (trade study, calculations, plots, references)

## Notes
This repo is intended as a portfolio artifact. If additional source code/notebooks are added later, they should live under a `/code` or `/notebooks` folder alongside the report.
