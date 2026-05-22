Fano 2-22 identity Feynman Graphon - Complete archive

This repository contains the complete material for the paper:

Fano 2-22 is the Feynman graphon: emergence of FLRW spacetime from a no-free-parameter algebraic construction

Author: Massimiliano Blandino
ORCID: https://orcid.org/0009-0006-3252-4011
Zenodo concept DOI: 10.5281/zenodo.19802606 (Alpha Series)
Zenodo concept DOI: 10.5281/zenodo.19955544 (Fano Series)


Repository structure

Fano_2-22_identity_Feynman_Graphon_Complete_archive/
├── paper/
│   ├── Fano_2-22_Feynman_graphon.tex      # LaTeX source
│   ├── Fano_2-22_Feynman_graphon.pdf      # Compiled manuscript
│   └── references.bib                     # Bibliography
├── code/
│   └── Fano_2-22_Feynman_Graphon_Verification_Suite.py
├── README.md
├── requirements.txt
└── LICENSE


Run the verification suite

Step 1: Clone the repository
git clone https://github.com/massimilianoblandino/Fano_2-22_identity_Feynman_Graphon_Complete_archive.git
cd Fano_2-22_identity_Feynman_Graphon_Complete_archive

Step 2: Install dependencies
pip install -r requirements.txt

Step 3: Run the verification script
cd code
python Fano_2-22_Feynman_Graphon_Verification_Suite.py

Expected runtime: about 10 seconds


Figures generated

The verification suite automatically generates three figures (saved in the same directory as the script):

cut_norm_convergence.png
  - Content: Cut norm vs refinement level k (log-log)
  - Message: Exponential decay O(2^{-k}) – confirms Theorem 4.3

gh_convergence.png
  - Content: Gromov-Hausdorff distance vs k (log-log)
  - Message: Exponential decay O(2^{-k}) – confirms Theorem B (Appendix)

spectral_ratio.png
  - Content: lambda1/lambda0 vs gamma R
  - Message: Asymptotic approach to 2 – confirms spectral rigidity

Note: Figures are not versioned in this repository. They are generated on-the-fly when running the verification script, ensuring perfect consistency between code and output.


Requirements

- Python 3.11 or higher
- numpy >= 1.24.0
- scipy >= 1.10.0
- matplotlib >= 3.7.0

Install all dependencies with:
pip install numpy scipy matplotlib


Key numerical results

gamma (geometric threshold) ................. 22.732171152303
kappa (contact coupling) ................... 2.291518179460
I0 (reference integral) .................... 5.48677492e-06
I1 (reference integral) .................... 5.48033080e-06
lambda1/lambda0 (practical) ................ 0.998825517553
lambda1/lambda0 (operator) .................. 1.997651035107
Asymptotic limit (gamma R -> infinity) ...... 2.0

Cut norm convergence (Monte Carlo)

k = 0
  Cut norm ...... 4.99e+00
  Normalized .... 1.0000
  Theoretical 2^{-k} .. 1.00
  Ratio ......... 1.000

k = 1
  Cut norm ...... 1.61e+00
  Normalized .... 0.3222
  Theoretical 2^{-k} .. 0.50
  Ratio ......... 0.644

k = 2
  Cut norm ...... 7.00e-01
  Normalized .... 0.1403
  Theoretical 2^{-k} .. 0.25
  Ratio ......... 0.561

The Monte Carlo estimation confirms the expected O(2^{-k}) decay trend.
The discrepancy between absolute values and the theoretical upper bound is due to the difficulty of sampling the supremum in a 2^N configuration space and does not affect the validity of Theorem 4.3, which is proven analytically.


Reproducibility

- Random seed is fixed: 20260522
- All numerical integrals use adaptive Gauss-Kronrod quadrature (absolute tolerance 1e-12)
- The code is fully deterministic and produces identical outputs on any system


License

This work is licensed under a Creative Commons Attribution 4.0 International License (CC BY 4.0).
You are free to share and adapt the material, provided you give appropriate credit to the author.

https://creativecommons.org/licenses/by/4.0/


Citation

If you use this work in your research, please cite:

@article{blandino2026fano,
  author    = {Blandino, Massimiliano},
  title     = {Fano 2-22 is the Feynman graphon: emergence of FLRW spacetime from a no-free-parameter algebraic construction},
  year      = {2026},
  doi       = {https://doi.org/10.5281/zenodo.20349651}
}


Contact

For questions or comments, please open an issue on GitHub or contact the author via ORCID.


This repository is part of the Alpha+Fano Series.
Complete series available at: 10.5281/zenodo.19802606
