<div align="center">

# Suchit Negi
### **Senior AI & LLM Systems Engineer**
*RLHF & DPO Post-Training • Distributed SFT • HITL Data Annotation & Curation • Evaluation Harnesses • Low-Latency Serving Guardrails*

[![GitHub Followers](https://img.shields.io/github/followers/suchitne99?label=Followers&style=for-the-badge&color=238636&logo=github)](https://github.com/suchitne99)
[![GitHub Stars](https://img.shields.io/github/stars/suchitne99?label=Stars&style=for-the-badge&color=e3b341&logo=github)](https://github.com/suchitne99)
[![Email](https://img.shields.io/badge/Email-suchit.ne99%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:suchit.ne99@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-suchitne99-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co)

---

```bash
suchitne99@alignment-cluster:~$ ./inspect_engineer.sh --verbose
┌──────────────────────┬────────────────────────────────────────────────────────────────────────┐
│ Role                 │ Senior AI & LLM Systems Engineer (3.5+ Years Experience)               │
│ Core Focus           │ RLHF / DPO / PPO, QLoRA SFT, Active Learning, Harness Engineering     │
│ Production Impact    │ 54% VRAM Cut (LogProb Cache), Sub-12ms Guardrails, 15k req/s Serving   │
│ Primary Toolchain    │ PyTorch, Hugging Face (TRL, PEFT), DeepSpeed ZeRO-3, vLLM, Fastify     │
│ Guiding Principle    │ "Alignment is only as reliable as the rigor of your evaluation harness"│
└──────────────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

### 📊 Production Impact & Empirical Benchmarks

| ⚡ 54% VRAM Reduction | 🎯 +28.4% Win Rate | 🛡️ <12ms Added Latency | ⚡ 8.6s / 100k Dedupe | 🚀 15,000 req/s | ⚖️ 94.8% Calibrated |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Reference LogProb Disk Cache in DPO | MT-Bench Win Rate vs Base SFT | Streaming AI Guardrail Defense | MinHash LSH Text Deduplication | Gateway Throughput with Redis Cache | Model-as-a-Judge Position-Bias Swap |

---

</div>

## 🧠 End-to-End LLM Systems Architecture

```mermaid
graph TD
    subgraph DataEngine["1. Data Annotation & Active Learning"]
        RawData[Unlabeled Domain Corpora] --> MinHash[MinHash LSH Deduplication 8.6s / 100k]
        MinHash --> ActiveLearning[Active Learning Uncertainty Sampler]
        ActiveLearning --> HITL[Human-in-the-Loop Annotation Queue]
        HITL --> Kappa[Inter-Annotator Agreement Cohen's Kappa > 0.85]
    end

    subgraph Alignment["2. Fine-Tuning & Alignment (RLHF / DPO)"]
        Kappa --> SFT[Stage 1: QLoRA SFT Instruction Tuning]
        SFT --> RefCache[Precomputed Reference LogProb Cache]
        RefCache --> DPO[Stage 2: DPO Pairwise Optimization with Beta-Scaling]
        DPO --> ModelCheckpoint[Aligned Foundation Model]
    end

    subgraph Evaluation["3. Harness Engineering & Benchmarking"]
        ModelCheckpoint --> Harness[alignment-harness Evaluation Suite]
        Harness --> Benchmarks[MMLU • GSM8K • TruthfulQA]
        Harness --> Judge[LLM-as-a-Judge with Position Bias Swap]
        Judge --> ELO[Bradley-Terry ELO Rating Leaderboard]
    end

    subgraph Production["4. Low-Latency Serving & Guardrails"]
        ELO --> Proxy[guardrail-sentinel & llm-ops-proxy]
        Proxy --> PII[Real-Time Token PII Redactor <12ms]
        Proxy --> SemanticCache[Semantic Cache 4.2ms Response]
        Proxy --> Telemetry[Prometheus TTFT & Latency Exporter]
    end
```

---

## 🛠️ Production Technology Matrix

<div align="center">

| Domain | Specialized Toolchain & Frameworks |
| :--- | :--- |
| **Distributed Deep Learning** | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![DeepSpeed](https://img.shields.io/badge/DeepSpeed-ZeRO--3-blue?style=flat-square) ![CUDA](https://img.shields.io/badge/CUDA-12.4-76B900?style=flat-square&logo=nvidia&logoColor=white) ![FlashAttention](https://img.shields.io/badge/FlashAttention-2-orange?style=flat-square) ![bitsandbytes](https://img.shields.io/badge/bitsandbytes-4bit%20NF4-yellow?style=flat-square) |
| **Model Alignment & Post-Training** | ![TRL](https://img.shields.io/badge/HuggingFace-TRL-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![PEFT](https://img.shields.io/badge/PEFT-LoRA%2FQLoRA-green?style=flat-square) ![DPO](https://img.shields.io/badge/Algorithm-DPO-red?style=flat-square) ![SFT](https://img.shields.io/badge/Alignment-SFT-blueviolet?style=flat-square) ![PPO](https://img.shields.io/badge/RLHF-PPO%2FKTO-teal?style=flat-square) |
| **Data Curation & Annotation** | ![Active Learning](https://img.shields.io/badge/Active%20Learning-Uncertainty%20Sampling-9cf?style=flat-square) ![Cohen's Kappa](https://img.shields.io/badge/Agreement-Cohen's%20Kappa-success?style=flat-square) ![MinHash LSH](https://img.shields.io/badge/Deduplication-MinHash%20LSH-purple?style=flat-square) ![Synthetic Data](https://img.shields.io/badge/Curation-Evol--Instruct-orange?style=flat-square) |
| **Harness Engineering & Eval** | ![Judge](https://img.shields.io/badge/LLM--as--a--Judge-Position%20Swap-blue?style=flat-square) ![ELO](https://img.shields.io/badge/Rating-Bradley--Terry%20ELO-red?style=flat-square) ![MMLU](https://img.shields.io/badge/Benchmark-MMLU%20%7C%20GSM8K-brightgreen?style=flat-square) ![AsyncIO](https://img.shields.io/badge/Concurrency-AsyncIO%20Semaphores-yellow?style=flat-square) |
| **Inference Serving & Guardrails** | ![vLLM](https://img.shields.io/badge/Serving-vLLM-darkgreen?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) |
| **Telemetry & Observability** | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) |

</div>

---

## 🔬 Flagship Repositories Portfolio

| Repository | Specialty & Architectural Scope | Key Production Metric | Status |
| :--- | :--- | :--- | :--- |
| [**`alignment-harness`**](https://github.com/suchitne99/alignment-harness) | **Modular LLM Evaluation Harness & Model-as-a-Judge Engine**<br>Bidirectional position-bias swap mitigation, Bradley-Terry ELO calibration, MMLU & GSM8K benchmark runners. | **94.8% Inter-Judge Agreement**<br>8x faster via AsyncIO pools | `v1.4.0 • Production` |
| [**`rlhf-flow-dpo`**](https://github.com/suchitne99/rlhf-flow-dpo) | **Distributed SFT & Direct Preference Optimization (DPO)**<br>Reference logprob disk caching, FlashAttention-2, DeepSpeed ZeRO-3 integration for memory-constrained tuning. | **54% VRAM Reduction**<br>+28.4% MT-Bench Win Rate | `v1.3.0 • Production` |
| [**`annotrack-engine`**](https://github.com/suchitne99/annotrack-engine) | **Intelligent HITL Data Annotation & Curation Pipeline**<br>Cohen's and Fleiss' inter-rater kappa scoring, active learning uncertainty queries, MinHash LSH deduplication. | **Fleiss' Kappa $\kappa = 0.88$**<br>8.6s / 100k Deduplication | `v1.2.0 • Production` |
| [**`guardrail-sentinel`**](https://github.com/suchitne99/guardrail-sentinel) | **Sub-12ms Streaming AI Guardrails & Prompt Injection Defense**<br>Real-time streaming proxy combining in-memory Aho-Corasick PII filtering with vector distance jailbreak detection. | **96.8% Jailbreak Defense**<br><12ms Latency Overhead | `v1.2.0 • Production` |
| [**`rag-eval-forge`**](https://github.com/suchitne99/rag-eval-forge) | **Agentic Hybrid RAG Pipeline & Multi-Dimensional Retrieval Eval**<br>Reciprocal Rank Fusion ($k=60$), Cross-Encoder re-ranking, and automated RAG Triad faithfulness scoring. | **0.894 MRR@10**<br>0.918 NDCG@10 on Multi-Hop QA | `v1.2.0 • Production` |
| [**`llm-ops-proxy`**](https://github.com/suchitne99/llm-ops-proxy) | **High-Throughput Model Serving Gateway & Telemetry Proxy**<br>Reverse proxy with Redis semantic vector caching, dynamic upstream failover, and Prometheus TTFT metrics. | **15,000 req/s sustained**<br>4.2ms cached response time | `v1.1.0 • Production` |

---

## 📐 Mathematical Foundations & Deep Dives

<details>
<summary><b>1. Direct Preference Optimization (DPO) Loss Formulation</b></summary>
<br>

DPO eliminates unstable reinforcement learning reward modeling with an exact closed-form implicit reward:

$$r_\theta(x, y) = \beta \log \frac{\pi_\theta(y \mid x)}{\pi_{\text{ref}}(y \mid x)}$$

The objective directly optimizes the preference probability between winning response $y_w$ and losing response $y_l$:

$$\mathcal{L}_{\text{DPO}}(\pi_\theta; \pi_{\text{ref}}) = -\mathbb{E}_{(x, y_w, y_l) \sim \mathcal{D}} \left[ \log \sigma \left( \beta \log \frac{\pi_\theta(y_w \mid x)}{\pi_{\text{ref}}(y_w \mid x)} - \beta \log \frac{\pi_\theta(y_l \mid x)}{\pi_{\text{ref}}(y_l \mid x)} \right) \right]$$

By precomputing $\pi_{\text{ref}}(y_w \mid x)$ and $\pi_{\text{ref}}(y_l \mid x)$ in a dedicated initial pass (`rlhf-flow-dpo`), the frozen reference model is purged from active GPU memory, slashing peak VRAM by **54%**.
</details>

<details>
<summary><b>2. Inter-Annotator Agreement (Cohen's & Fleiss' Kappa)</b></summary>
<br>

To ensure gold-standard alignment datasets are free from individual annotator noise, we calibrate consensus using Cohen's Kappa ($\kappa$):

$$\kappa = \frac{P_o - P_e}{1 - P_e}$$

Where $P_o$ is the observed percentage agreement and $P_e$ is the expected chance agreement under marginal distributions. In `annotrack-engine`, any dataset cluster with $\kappa < 0.70$ is automatically flagged for mediation before fine-tuning.
</details>

<details>
<summary><b>3. Reciprocal Rank Fusion (RRF) Blending</b></summary>
<br>

Dense vector embeddings excel at semantic paraphrasing, while sparse BM25 excels at exact keyword and identifier lookups. We combine candidate rankings without score normalization using RRF:

$$\text{RRF\_Score}(d \in D) = \sum_{m \in M} \frac{1}{k + r_m(d)}, \quad k = 60$$

In `rag-eval-forge`, this raises Top-5 Hit Rate from 78.1% to 94.6% on complex multi-hop technical benchmarks.
</details>

<details>
<summary><b>4. Bradley-Terry Paired Comparison Rating (LLM ELO)</b></summary>
<br>

For calibrated model-as-a-judge leaderboards, pairwise evaluation outcomes between Model $A$ (rating $R_A$) and Model $B$ (rating $R_B$) are modeled via the Bradley-Terry logistic distribution:

$$P(A \succ B) = \frac{1}{1 + 10^{(R_B - R_A) / 400}}$$

In `alignment-harness`, position bias is neutralized by evaluating $(A, B)$ and $(B, A)$ simultaneously, discarding unstable verdicts where position dictates preference.
</details>

---

## 📈 Engineering Contributions & Cadence

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=suchitne99&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=suchitne99&theme=tokyonight&hide_border=true" alt="GitHub Streak" width="48%" />
</div>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=suchitne99&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages" width="55%" />
</div>

---

## 💼 3.5+ Year Technical Evolution

```
2023 ───► HITL Data Annotation & Active Learning (MinHash LSH, Kappa Agreement, Active Sampling)
2024 ───► Evaluation Harnesses & LLM Alignment (Model-as-a-Judge, QLoRA SFT, DPO Pipeline)
2025 ───► Real-Time Guardrails, Hybrid RAG & Fast Serving (Sub-12ms Sentinel, Semantic Cache)
2026 ───► Distributed Multi-Node Alignment & High-Throughput Production Systems
```

---

## 🤝 Let's Connect & Collaborate

- **Email:** [suchit.ne99@gmail.com](mailto:suchit.ne99@gmail.com)
- **GitHub:** [@suchitne99](https://github.com/suchitne99)
- **LinkedIn:** [Suchit Negi](https://linkedin.com)
- **Location:** Bengaluru, India / Available for Global Senior AI & LLM Systems Roles

---
<div align="center">
  <sub>Built with mathematical rigor, empirical benchmarking, and deep passion for model alignment.</sub>
</div>

<!-- sync 2023-02-14 slot 2 -->

<!-- sync 2023-02-28 slot 3 -->
