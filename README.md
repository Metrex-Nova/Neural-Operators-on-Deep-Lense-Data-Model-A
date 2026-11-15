# DeepONet Architecture Ablation on DeepLense Model A

An ablation of **14 operator-learning architectures** on the ML4SCI DeepLense *Model A* gravitational-lensing dataset. Most are variants of DeepONet that change only the branch or trunk network, so the comparison isolates which design choices matter for lensing fields.

## Architectures

**Base model** (`Deeponet Architectures/`)
1. Vanilla DeepONet

**Ablations** (`Architecture Ablation on Model A/`)

| # | Variant | What changes |
|---|---|---|
| 2 | Stacked DeepONet | One branch network per output basis |
| 3 | Convolutional DeepONet | CNN branch for image inputs |
| 4 | POD-DeepONet | Trunk replaced by a POD basis from training data |
| 5 | Fourier DeepONet | Fourier-feature trunk |
| 6 | Attention DeepONet | Attention in the branch |
| 7 | Fourier Neural Operator | Non-DeepONet reference |
| 8 | Gated Multi-Scale Fourier-DeepONet | Gated multi-scale Fourier features |
| 9 | MIONet | Multiple-input operator network |
| 10 | Haar-wavelet DeepONet | Haar wavelet basis |
| 11 | Coiflet-wavelet DeepONet | Coiflet wavelet basis |
| 12 | Daubechies-wavelet DeepONet | Daubechies wavelet basis |
| 13 | Multi-output DeepONet | Shared trunk, several outputs |
| 14 | BelNet | Learned sensor locations |

## Running

The scripts were written for Kaggle and look for the dataset (with its `manifest.csv`) under `/kaggle/input`. To run elsewhere, change `find_dataset_root` at the top of the script.

## Related work

This was exploratory work for my GSoC 2026 project with ML4SCI. The final architectures and the multi-seed benchmark are in [GSOC-finalSubmission](https://github.com/Metrex-Nova/GSOC-finalSubmission) and [Neural_operators_for_lensing_and_pde_benchmarks](https://github.com/Metrex-Nova/Neural_operators_for_lensing_and_pde_benchmarks).

## Author

Paras Balani, BITS Pilani, Hyderabad Campus.
