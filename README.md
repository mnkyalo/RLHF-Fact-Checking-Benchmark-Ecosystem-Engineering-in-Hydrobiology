# RLHF & Fact-Checking Benchmark: Ecosystem Engineering in Hydrobiology 🌊🧪

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=flat&logo=github)](https://github.com/mnkyalo/RLHF-FactChecking-Benchmark-Hydrobiology)
[![Format](https://img.shields.io/badge/Data_Format-Label_Studio_RLHF_JSON-blue)](#)
[![Domain](https://img.shields.io/badge/Domain-LLM_Alignment_%2F_Stream_Ecology-green)](#)

## Overview
This case study presents a domain-specific **Reinforcement Learning from Human Feedback (RLHF)** and fact-checking benchmark designed for evaluating Large Language Models (LLMs) on specialized STEM topics. By auditing model generations on beaver reintroduction (*Castor fiber / Castor canadensis*) against peer-reviewed stream ecology literature, this framework mitigates hallucination propagation in high-liability scientific knowledge retrieval systems.

---

## Key Features & Evaluation Specs
* **Evaluator:** Margaret Kyalo
* **Task Type:** Pairwise Preference Ranking, Domain-Specific Hallucination Detection, & Critical Evaluation
* **Domain:** Stream Ecology, Freshwater Biology, & Hydrobiology
* **Primary Objective:** Detect and flag subtle, plausible-sounding domain hallucinations (such as fabricated thermal regimes or flawed biogeochemical claims) to ensure safety and precision in specialized LLM outputs.

---

## Benchmark Case Study

### Evaluation Prompt
> *"Explain how reintroducing beavers (Castor fiber / Castor canadensis) alters the hydrobiology and benthic ecology of a degraded headwater stream."*

### Model Comparison & Pairwise Preference

* **Winning Response:** `Response A`
* **Preference Margin:** Significantly Better

| Evaluated Model Output | Status | Ecological Accuracy & Key Findings |
| :--- | :--- | :--- |
| **Response A** | **Accepted** | Correctly distinguishes lotic-to-lentic transitions, macroinvertebrate shifts (rheophilic to limnophilic taxa), and landscape-scale (gamma) biodiversity dynamics. |
| **Response B** | **Rejected** | Failed critical verification. Displayed 4 major scientific hallucinations across hydrology, thermal dynamics, fisheries biology, and biogeochemistry. |

---

## Hallucination & Factual Error Breakdown (Response B)

1. **Hydrological Misconception:** Claimed dams *"completely stop erosion and eliminate downstream flooding."*
   * *Correction:* Dams attenuate and delay flood peaks; leaky structures do not eliminate flooding entirely.
2. **Thermal Regime Fabrication:** Claimed ponds raise water temperatures by $10-15^\circ\text{C}$ across the entire river basin.
   * *Correction:* Local thermal buffering occurs, but a $10-15^\circ\text{C}$ basin-wide increase would be ecologically catastrophic.
3. **Fisheries Biology Error:** Claimed warm water creates ideal conditions for cold-water salmonids (trout/salmon).
   * *Correction:* Salmonids require cold, oxygenated water; excessive warming induces severe physiological stress.
4. **Biogeochemical Hallucination:** Claimed ponds eliminate greenhouse gas emissions by permanently sealing organic matter.
   * *Correction:* Impounded wetlands increase localized anaerobic decomposition, frequently elevating methane ($\text{CH}_4$) emissions.

---

## Evaluation Workspace

![Label Studio RLHF Interface](assets/label_studio_interface.png)
*Figure 1: Custom Label Studio RLHF interface displaying side-by-side model outputs, multi-select hallucination flags, and structured critique input fields.*

---

## Production & Safety Impact
By applying strict scientific auditing to specialized domain data, this workflow prevents plausible-sounding factual fabrications from entering model training pipelines. This high-fidelity preference data directly supports building robust safety guardrails for RLHF alignment—prioritizing factual integrity over conversational fluency.
