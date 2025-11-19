# Santa 2025 - Christmas Tree Packing Challenge V1

This repository contains my approach for the [Santa 2025 - Christmas Tree Packing Challenge](https://www.kaggle.com/competitions/santa-2025) on Kaggle.

## Overview

The objective of this challenge is to optimally pack rotatable Christmas trees (polygonal shapes) into the smallest possible square, minimizing the bounding box area for each value of N (number of trees from 1 to 200). The final solution is evaluated by an ensemble score that combines all cases.

**Notebook Link**: [Santa 2025 - Christmas Tree Packing Challenge V1](https://www.kaggle.com/code/adityapawar327/santa-2025-christmas-tree-packing-challenge-v1)

**Public Score**: 85.92

## Table of Contents

- Library Imports and Environment Setup
- Global Configuration and Precision Settings
- ChristmasTree Class Definition
- Utility Functions (Scoring/Collision)
- Simulated Annealing Algorithm (N < 20)
- Grid Search Algorithm (N >= 20)
- Hybrid & Ensemble Solvers
- Main Computation Loop (N = 1 to 200)
- Submission Formatting and Export

## Methodology

- **Small N (< 20):** Uses Simulated Annealing for efficient search in small configuration spaces.
- **Large N (>= 20):** Uses a tailored Grid Search for tractable solution space exploration.
- **Hybrid/Ensemble:** Runs multiple seeds and chooses the best solution for each N.
- **Collision Detection:** Employs Shapely geometry operations to prevent tree overlap.
- **Performance:** Code leverages parallelization (`ProcessPoolExecutor`) and high-precision (Decimal) arithmetic.

## Usage

1. Install dependencies:
   - `shapely`, `numpy`, `pandas`, `matplotlib`, `tqdm`

2. Run the notebook or script sequentially to output results and save a `submission.csv`.

3. Check the score on important N cases (e.g., 1, 10, 25, 50, 100, 150, 200).

## Output

- The notebook prints key logs during computation.
- A `submission.csv` is generated with columns: `id`, `x`, `y`, `deg` (example row: `001_0, s-9.146226, s-0.12832, s-224.999647`).

## License

This project is released under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).

## Author

Aditya Pawar ([Kaggle Profile](https://www.kaggle.com/adityapawar327))

---

For questions or collaboration, feel free to reach out via Kaggle discussions or connect on [LinkedIn](https://www.linkedin.com/in/adityapawar327).
