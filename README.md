
# Stormwatch Harbour — Agentic AI Assignment 2

This project simulates a harbour where dockworkers deliver cargo from ships to a warehouse. The agents make decisions about which ship to serve and how to respond to storm warnings.

## Scenario settings

The simulation uses these settings:

- Grid size: 24 × 16 cells
- Dockworkers: 12
- Ship arrival interval: 6–10 ticks
- Storms per run: 3
- Cargo per ship: 10 units
- Simulation length: 600 ticks
- Berths: B1, B2, B3 and B4
- Warehouse: (0, 15)

The simulation uses the student ID suffix 5 settings provided for the assignment.

## Agent policies

The simulation includes four non-LLM policies:

- **Baseline:** Workers do not move or deliver cargo.
- **Reflex:** Workers choose a ship using the information currently available and respond to storm warnings.
- **Model-based:** Workers keep information about berth conditions and storm warnings.
- **Utility:** Workers compare possible choices using cargo, distance, nearby workers and storm risk.

## Project files

- `run.py` — runs one simulation using a chosen policy and seed.
- `b3_analysis.py` — runs the berth-balancing comparison for seeds 11–20.
- `source/` — simulation source code, if included in this repository.
- `results/` — CSV files and figures produced by the experiments.
- `Stormwatch_Harbour_Kaggle.ipynb` — Kaggle notebook with the analysis and LLM prompt test, if included.

## Setup

Use Python 3.10 or later. Install the required packages:

```bash
pip install -r requirements.txt
