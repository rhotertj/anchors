# Anchors

Implementation and Extensions of [Anchors](https://homes.cs.washington.edu/~marcotcr/aaai18.pdf)

## Content
 * [X] Reproduction (10): Implement Anchors via the Bottom-up Construction approach.
 * [X] Extension (10): Implement Beam Search on top of the Bottom-up Construction.
 * [X] Analysis (5): Perform an analysis on how 𝐵, 𝛿 and 𝜖 influence the results.
 * [X] Alternative Optimizer (10): Replace Beam Search/Bottom-up Construction with SMAC
(Bayesian Optimization)

References:
* Paper Reference: https://homes.cs.washington.edu/~marcotcr/aaai18.pdf
* (Original) Code Reference: https://github.com/marcotcr/anchor

## Installation

Create a conda environment
  ```bash
 $ conda env create
 $ conda activate ginger-anchors
  ```
  *Note: swig is needed to install smac3. See [installation instructions](https://automl.github.io/SMAC3/master/pages/getting_started/installation.html).*


## Usage

You can get an explanation by setting up an Explainer and calling one of three search functions.

```python
exp = Explainer(X_df)
anchor = exp.explain_bottom_up(instance, model, tau=0.95)
print(anchor.get_explanation())

```

For a more detailed example, see [src/main.py](https://github.com/rhotertj/anchors/blob/master/src/main.py).

## Analysis

The plots were too large to put them into this repository. Please download them from [seafile](https://seafile.cloud.uni-hannover.de/d/1ba613292c774f8c87dc/).

To reproduce the raw data, run:

```bash
ginger-anchors> python src/analysis.py
```
A preview can be found in our writeup: [analysis.md](https://github.com/rhotertj/anchors/blob/master/analysis.md)

## Authors
[Jim Rhotert](https://github.com/Dschimm) & [Julian Bilsky](https://github.com/julianbil)

