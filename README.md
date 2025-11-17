# Reaction–Diffusion Exchange Economies with Aggregated Cobb–Douglas Preferences

This repository formalizes an extension of the two-good convex zero-sum optimal exchange model introduced in [Emergent Properties of Distributed Agents with Two-Stage Convex Zero-Sum Optimal Exchange Network](https://github.com/onedge-network/Emergent_Properties_paper) into an \(n\)-good setting. It introduces a globally consistent method for aggregating **pairwise Cobb–Douglas preference functions** into an agent-specific exponent vector that maintains convexity, exchange efficiency, and tractability even in high-dimensional economic systems.

The resulting framework is interpreted as a **Reaction–Diffusion Economy**, where:
- **Reaction phase**: Each agent transforms its internal endowment using agent-specific production rules (modeled as linear technologies).
- **Diffusion phase**: Agents strategically exchange their holdings to maximize utility using their aggregated Cobb–Douglas preferences under a global price vector.

---

## 📘 Key Contributions

- ✅ **Pairwise to Global Preference Aggregation**: A rigorous method to infer globally consistent Cobb–Douglas exponent vectors $`(\boldsymbol{\beta}_i)`$ from a matrix of pairwise Cobb–Douglas preferences $`(\alpha_{ij})`$, provided a cycle consistency condition is met.

- ✅ **Extension to Arbitrary Number of Goods $`(n \geq 2)`$**: Preserves convexity, feasibility, and budget balance from the original two-good model while allowing complex specialization dynamics and price feedback.

- ✅ **Reaction–Diffusion Interpretation**: Inspired by Turing’s model of morphogenesis, the system enables emergent pattern formation in economic allocation by alternating production and exchange steps in discrete rounds.

  - ✅ **Closed-form Marshallian Demand + Utility Derivatives**: Exchange solutions are based on closed-form Marshallian demand equations, with a 1D concave utility optimization over $`(\lambda_i)`$ (the exchange fraction), ensuring numerical simplicity.

---

## 📄 Included Files

| File | Description |
|------|-------------|
| `LaTeX/Reaction_Diffusion_Economy.tex` | LaTeX source for the extended \(n\)-good model |
| `LaTeX/Reaction_Diffusion_Economy.pdf` | Last rendered pdf version of the paper "Reaction–Diffusion Exchange Economies with Aggregated Cobb–Douglas Preferences for n ≥2 Good" (Tristain 2025) |
| `LaTeX/references.bib` | BibTeX file including citations to Tristain (2024), Turing (1952), and related references |
| `README.md` | This project overview |

---

## 📐 Mathematical Model

Given pairwise Cobb–Douglas preference parameters:
$`\alpha_{ij} \in (0,1), \quad \text{with } \alpha_{ji} = 1 - \alpha_{ij}`$

We define:
$`r_{ij} = \frac{1 - \alpha_{ij}}{\alpha_{ij}} \quad \Rightarrow \quad \frac{\beta_j}{\beta_i} = r_{ij}`$

A consistent global utility:
$`u(\mathbf{x}) = \prod_{k=1}^n x_k^{\beta_k}`$

exists **if and only if** all directed cycles satisfy:
$`\prod_{\text{cycle}} r_{ij} = 1`$

---
