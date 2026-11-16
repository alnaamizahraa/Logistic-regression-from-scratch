# Logistic Regression from Scratch

A Break Through Tech AI coursework project by **Zahraa Al-Naami**, implementing binary logistic regression with NumPy and comparing its fitted coefficients and runtime with scikit-learn.

## Project overview
The prediction target is Airbnb host superhost status. Seven features describe review ratings, cleanliness, check-in, communication, value, response rate, and acceptance rate. The course supplied preprocessed data.

## Implementation and contribution
Completed the lab's sigmoid, gradient, Hessian, Newton update, and convergence logic within course-provided scaffolding; fitted the scratch and reference models and recorded coefficient and runtime comparisons. This repository preserves that implementation in a notebook reconstructed from an HTML export. AI assistance was used for reconstruction and portfolio documentation.

## Recorded findings
| Measurement | Scratch implementation | scikit-learn |
|---|---:|---:|
| First coefficient | 0.56690005 | 0.56691547 |
| Intercept | -1.829062262272181 | -1.82906726 |
| Fit time, mean ± standard deviation | 296 ± 153 ms | 333 ± 78 ms |

Timings are historical, environment-dependent measurements from 7 runs with 1 loop each. Variability overlaps; no reliable speed advantage is claimed. Coefficient similarity is a limited implementation comparison, not held-out predictive evaluation.

## Files
- `logistic-regression-from-scratch.ipynb`: annotated model code, recovered text outputs, interpretation, and limitations.
- `requirements.txt`: required packages (original versions unknown).

## Setup and run
1. Install Python 3 and create a virtual environment.
2. Install dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```
3. Obtain the authorized course `airbnbData_train.csv` and place it in a `data` directory beside the notebook.
4. Start Jupyter from the repository directory:
   ```bash
   jupyter notebook
   ```
5. Open the notebook and run its cells in order. The last benchmark cells use IPython `%timeit`.

**Data availability:** the CSV is not included, and a public source for this exact preprocessed file has not been verified. New users cannot reproduce the original-data results without obtaining it. Synthetic data is not supplied as if it were the original. The original dependency versions were not preserved, so runtime and library behavior may differ.

## Reconstruction and validation
The original course workspace is inaccessible. The notebook was reconstructed from the saved HTML export. One malformed feature-selection line was repaired by restoring `feature_list` before `= [...]`. Code syntax was checked, but the original-data experiment has **not** been rerun. Outputs are preserved historical results. Blank course analysis and reflection prompts were omitted; added interpretation is labeled as portfolio commentary.

## Limitations
- All examples are used for fitting; no train/test split or held-out prediction metrics are reported.
- The optimizer is Newton's method, not ordinary first-order gradient descent.
- Explicit Hessian inversion and normalized-weight convergence checks require more robust handling of singular matrices and zero vectors.
- The preserved implementation sets final coefficient attributes only after convergence; iteration-limit handling needs improvement.
- This is an educational implementation, not a production-ready classifier.

## Next steps
Recover authorized data, record dependency versions, add convergence and numerical tests, replace explicit inversion with a stabilized solve, handle the iteration limit, and evaluate generalization with properly separated training, validation, and test data.

## Attribution
Based on Break Through Tech AI Lab 4, “ML Life Cycle: Modeling — Building a Logistic Regression Model From Scratch.” The exercise, scaffolding, and dataset were course-provided. No license over the course materials or dataset is asserted here.
