# Tahereh Vasei

**Ph.D. Candidate in Electrical Engineering — New York Institute of Technology**

I work on making machine learning reliable on noisy, real-world signals: deep learning for multi-site biomedical data, RTL design and verification, and LLM agents for hardware design automation. My research asks a simple question in three different settings — *is the model learning the signal, or the source of the data?*

---

## Featured Research

### 1. Reference-Conditioned CVAE Harmonization for Multi-Cohort EEG Classification

**Ph.D. research · Status: manuscript under revision**

EEG recordings collected at different sites differ systematically, and a classifier can learn *which site* a recording came from instead of the diagnosis. I built an end-to-end pipeline — preprocessing, a reference-conditioned conditional variational autoencoder (CVAE), directed connectivity graphs (dPLI), and a GATv2 classifier — that removes cohort-specific signal before classification, evaluated with matched, subject-independent folds.

| | Before harmonization | After harmonization |
|---|---|---|
| Balanced accuracy (403 participants, 2 mixed-class cohorts) | 67.3% | **77.7%** |
| MCC | 0.368 | **0.530** |
| Source-cohort discriminator accuracy | 99.4% | **31.2%** |

- 817 participants · 6 cohorts · 32,987 EEG segments
- Three-way discriminator test (unharmonized / shuffled conditioning / true conditioning) to verify the conditioning — not the architecture alone — removes source information
- Stack: Python, PyTorch, PyTorch Geometric, MNE

### 2. Cross-Device Harmonization in Paired Dry/Gel EEG

**Ph.D. research · Status: manuscript in preparation**

Can a model trained on laboratory gel-electrode EEG be used on portable dry-electrode recordings of the *same people*? Using paired recordings from 35 participants and 316 connectivity features, I studied when statistical alignment between devices does — and does not — produce clinical transfer.

- Cross-device AUC improved from **0.549 (raw) to 0.742** after asymmetric harmonization (gel → dry)
- The reverse direction showed no benefit — transferability is directional, and stronger statistical alignment did not always mean better transfer
- Evaluation: participant-held-out folds, 200 full-pipeline label permutations, 2,000 participant bootstraps

### 3. VerifAgent-RL — Auditing an LLM Verification Agent

**Independent project · [Repository](https://github.com/Tvasei/VerifAI-Agent) · Paper submitted to ISQED 2027**

An LLM agent (local Qwen2.5-Coder-3B) that generates verification plans for an open-source UART core, scored by an automated judge in a Best-of-*K* loop. The agent's mean reward was +0.837 — implausibly good. I audited the trajectories and found the judge was crediting duplicate and overly broad claims; rescoring the unchanged runs under the corrected judge gave **+0.004**. The project became a failure-analysis study of how evaluation design inflates agent scores.

### 4. Wearable Brain–Computer Interface — Algorithm to RTL

**Published · M.Sc. research**

A complete motor-imagery BCI pipeline (IIR filtering → common spatial patterns → linear SVM) translated into a fixed-point RTL architecture using time sharing, RAM-based filter folding, and pipelining.

- **77.4%** classification accuracy · **45 nm CMOS** · **4 mW** · **0.25 mm²** · validated on Xilinx Virtex-7 FPGA
- 📄 Vasei, Saber, Nahvy & Navabi, *IET Computers & Digital Techniques*, 2024 — [doi.org/10.1049/2024/5596468](https://doi.org/10.1049/2024/5596468)

---

## Also on this profile

- **[EEG & BCI Research Portfolio](https://github.com/Tvasei/eeg-bci-research-portfolio)** — full project pages, figures, and results for the studies above

- **[3D Spatial Prefetcher](https://github.com/Tvasei/3d-spatial-prefetcher)** — SystemVerilog RTL design and class-based verification environment (100% functional coverage closure)
- **Parameterized UART** — SystemVerilog design and verification environment with SVA and coverage-driven closure (91.74% merged functional coverage)

## Tools I use

`Python` · `PyTorch` · `SystemVerilog / UVM` · `Verilog` · `Cocotb` · `MATLAB` · `Vivado` · `ModelSim / Questa` · `Git` · `Linux`

## Contact

- LinkedIn: [linkedin.com/in/tahere-vasei](https://www.linkedin.com/in/tahere-vasei)
- Email: taherevaseii@gmail.com
