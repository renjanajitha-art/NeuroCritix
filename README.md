# NeuroCritix
**Early Detection of Neurodegenerative Stress via Brain Criticality & EEG Complexity**

**Author:** Rejitha Renjan *(Independent Researcher | MSc Zoology)*  
**Live Interactive Prototype:** [Launch NeuroCritix App]([https://towering-neuro-scan-pulse.base44.app])  
**Status:** Research & Educational Prototype (November 2026)

---

## Overview
**NeuroCritix** is a computational neuroscience prototype designed to detect upstream functional stress in neural networks years before structural damage (such as amyloid plaques, tau tangles, or cortical atrophy) becomes visible on conventional MRI scans. 

By modeling the brain as a complex dynamical system operating near a critical phase transition, NeuroCritix tracks how mitochondrial bioenergetics and cellular negentropy erode under systemic stress.

---

## Core Scientific Framework

### 1. Brain Criticality & Negentropy
* **Brain Criticality:** Healthy neural networks operate near a critical boundary between rigid order and random chaos, maximizing information processing and dynamic range.
* **Negentropy & Bioenergetics:** Living neural circuits import free energy (ATP) to sustain organized electrical signaling. Mitochondrial failure triggers an *entropy cascade* across molecular, cellular, and network levels.

### 2. Quantitative EEG Complexity Metrics
NeuroCritix evaluates four key dynamical signatures from EEG signals:
* **Shannon Entropy (bits):** Measures signal unpredictability and information richness (~8.4 in healthy vs. ~2.8 in neurodegenerative profiles).
* **Lempel-Ziv (LZ) Complexity (0–1):** Quantifies algorithmic pattern diversity (~0.79 healthy vs. ~0.22 neurodegenerative).
* **Detrended Fluctuation Analysis (DFA) Exponent:** Captures long-range temporal correlations (healthy range ~0.50–0.75; abnormal shift to ~1.18).
* **Power-Law / 1/f Scaling Exponent ($\beta$):** Tracks large-scale network synchronization (~1.58 critical vs. ~0.74 decoupled).

---

## Stochastic Criticality Simulation Model
The **Brain Explorer** and **Compare** modules implement a bistable cubic stochastic differential equation integrated via the Euler-Maruyama method:

$$\frac{dx}{dt} = -x^3 + x + r + \sigma \xi(t)$$

* **$x$**: Brain negentropy-generating capacity (healthy baseline $x = 1.2$).
* **$r$**: Systemic load parameter (range $-0.5$ to $0.5$).
* **Critical Tipping Point ($R_{CRITICAL}$):** $\frac{2}{3\sqrt{3}} \approx 0.385$.
* **Hysteresis:** Perturbations below $R_{CRITICAL}$ (e.g., $r = 0.25$) remain reversible, whereas exceeding $R_{CRITICAL}$ (e.g., $r = 0.45$) eliminates the healthy attractor state, causing permanent collapse even after load decreases.

---

## Application Architecture
* **Home:** Scroll-driven neurobiology story from single neurons to the entropy cascade.
* **Brain Explorer:** Real-time bistable simulation with systemic load slider and acute perturbation ("Nudge") controls.
* **Upload & Dashboard:** EEG pipeline supporting 17 simulated profiles across 6 clinical/reference cohorts, complete with spectral charts, channel tables, and structural MRI reference ranges.
* **Compare:** Side-by-side hysteresis demonstration contrasting reversible psychiatric-like load vs. irreversible neurodegenerative collapse.
* **Learn:** Plain-language educational library with scientific references.

**Tech Stack:** React, Tailwind CSS, Recharts, Three.js, Base44.
[![DOI](https://zenodo.org)](https://doi.org)


---

## Disclaimer
*NeuroCritix is an independent research and educational prototype created for academic demonstration. All analyses and datasets are generated from synthetic simulations. It is not a medical device and must not be used for clinical diagnosis or patient care.*
