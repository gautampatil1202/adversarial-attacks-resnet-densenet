# Adversarial Attacks on ResNet-34 and Transferability to DenseNet-121

This project investigates the robustness of a pre-trained ResNet-34 model under adversarial attacks using a subset of ImageNet-1K, and evaluates the transferability of these attacks to another architecture, DenseNet-121.

## Project Tasks
- Evaluate ResNet-34 on a clean dataset to establish baseline accuracy.
- Implement Fast Gradient Sign Method (FGSM) and Projected Gradient Descent (PGD) attacks under L∞ constraints.
- Generate localized patch attacks targeting 32×32 regions.
- Measure top-1 and top-5 accuracy degradation across all attack types.
- Test transferability of adversarial examples on DenseNet-121.

## Results Summary

| Dataset                    | Top-1 Accuracy (ResNet) | Top-1 Accuracy (DenseNet) |
|----------------------------|--------------------------|----------------------------|
| Original (Clean)           | 76.00%                   | 74.80%                     |
| FGSM ($\epsilon$=0.02)     | 6.20%                    | 63.40%                     |
| PGD ($\epsilon$=0.02)      | 0.00%                    | 63.40%                     |
| Patch-PGD ($\epsilon$=0.3) | 45.40%                   | 67.80%                     |

