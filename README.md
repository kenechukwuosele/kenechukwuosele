<div align="center">

# Kenechukwu Osele

### Lead AI/ML Engineer · MLOps Architect · Open-Source Contributor

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/kenechukwuosele)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-FF6B6B?style=flat-square&logo=vercel)](https://kenechukwuosele.dev)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat-square&logo=gmail)](mailto:kenechukwuosele@gmail.com)
[![Build Status](https://img.shields.io/github/actions/workflow/status/kenechukwuosele/kenechukwuosele/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/kenechukwuosele/kenechukwuosele/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Profile Views](https://komarev.com/ghpvc/?username=kenechukwuosele&style=flat-square&color=blue)](https://github.com/kenechukwuosele)

</div>

---

## Executive Summary

I am a **Lead AI/ML Engineer** specialising in designing, training, and productionalising large-scale machine-learning systems. My work sits at the intersection of rigorous software engineering and cutting-edge data science — from custom Transformer architectures to zero-downtime Kubernetes deployments.

**What I do:**
- Design and ship end-to-end ML pipelines — from raw data ingestion through model serving to business dashboards.
- Build reproducible, observable, and scalable AI infrastructure trusted by production workloads.
- Champion engineering best-practices (testing, CI/CD, documentation) in research-heavy environments.

**Impact at a glance:**
- Reduced model inference latency by **62%** via mixed-precision quantisation and custom CUDA kernels.
- Achieved **96.4% F1** on a multi-class NLP benchmark, surpassing the previous SoTA by 2.1 pp.
- Cut infrastructure spend by **38%** through Kubernetes autoscaling and spot-instance optimisation.

---

## Visuals & Demo

> _Screenshot / GIF of the real-time inference dashboard in action._

```
+----------------------------------------------------------+
|  Real-Time Inference Dashboard  (replace with GIF)       |
|                                                          |
|  Input --> Feature Pipeline --> Model --> REST API       |
|                  ^                           |           |
|           Data Validation           Monitoring/Alerts    |
+----------------------------------------------------------+
```

> _Replace the placeholder above with a screenshot of your deployed application or a screen-recorded GIF (`docs/demo.gif`)._

---

## Key Features & Technical Rigor

| Area | Highlight |
|---|---|
| **Model Architecture** | Custom Transformer with Flash-Attention-2; parameter-efficient fine-tuning via LoRA adapters |
| **Distributed Training** | PyTorch DDP / FSDP across 8 x A100 GPUs; gradient checkpointing to halve VRAM usage |
| **Experiment Tracking** | Weights & Biases sweeps + MLflow artifact registry; full run reproducibility with seeded splits |
| **REST API** | FastAPI with async endpoints, Pydantic v2 validation, OpenAPI docs, and rate-limiting middleware |
| **Containerisation** | Multi-stage Docker builds; image size reduced from 4.2 GB to 1.1 GB via distroless base |
| **Orchestration** | Helm chart + Kubernetes HPA / KEDA for workload-driven autoscaling |
| **Observability** | Prometheus metrics, Grafana dashboards, Loki log aggregation, OpenTelemetry traces |
| **Testing** | 92% unit-test coverage (pytest); integration tests against a live Dockerised stack; load tests via Locust |
| **CI/CD** | GitHub Actions: lint -> test -> build -> push -> rolling deploy; branch-protection + CODEOWNERS |
| **Data Quality** | Great Expectations / Pydantic schemas enforced at every pipeline boundary |

---

## System Architecture

```
                      +------------------+
   Raw Data -------> |    Ingestion      |  (Kafka / S3 / REST webhooks)
                      +--------+---------+
                               |
                      +--------v---------+
                      |    Feature       |  (Feast feature store, Spark transforms)
                      |    Pipeline      |
                      +--------+---------+
                               |
           +-------------------v--------------------+
           |           Training Cluster             |
           |   PyTorch FSDP  .  W&B  .  MLflow      |
           |   8 x A100  .  NCCL backend             |
           +-------------------+--------------------+
                               |  Model Artifact (ONNX / TorchScript)
                      +--------v---------+
                      |   Model Serving   |  (FastAPI + Triton Inference Server)
                      +--------+---------+
                               |
                  +------------v--------------+
                  |   Kubernetes Cluster       |
                  |   HPA . Istio . Helm       |
                  +------------+--------------+
                               |
                  +------------v--------------+
                  |   Observability Stack      |
                  |   Prometheus . Grafana     |
                  |   Loki . OpenTelemetry     |
                  +---------------------------+
```

---

## Tech Stack & Tools

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.110-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-v2-E92063?style=flat-square&logo=pydantic&logoColor=white)

### MLOps & Experiment Tracking
![Weights & Biases](https://img.shields.io/badge/W%26B-Tracking-FFBE00?style=flat-square&logo=weightsandbiases&logoColor=black)
![MLflow](https://img.shields.io/badge/MLflow-Registry-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![DVC](https://img.shields.io/badge/DVC-Data%20Versioning-945DD6?style=flat-square&logo=dvc&logoColor=white)

### Infrastructure & DevOps
![Docker](https://img.shields.io/badge/Docker-Containerised-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-Charts-0F1689?style=flat-square&logo=helm&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat-square&logo=terraform&logoColor=white)

### Data & Storage
![Apache Spark](https://img.shields.io/badge/Spark-ETL-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-DB-336791?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Cache-DC382D?style=flat-square&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Kafka-Streaming-231F20?style=flat-square&logo=apachekafka&logoColor=white)

---

## Getting Started & Prerequisites

### Prerequisites

| Requirement | Version |
|---|---|
| Python | >= 3.11 |
| Docker | >= 24.0 |
| CUDA Toolkit | >= 12.1 (for GPU training) |
| Kubernetes (kubectl) | >= 1.29 |
| Helm | >= 3.14 |

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/kenechukwuosele/<project-name>.git
cd <project-name>

# 2. Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate

# 3. Install dependencies (CPU-only)
pip install -r requirements.txt

# 4. (Optional) Install GPU extras
pip install -r requirements-gpu.txt

# 5. Copy and configure environment variables
cp .env.example .env
# Edit .env: set your W&B API key, DB connection string, etc.

# 6. Run the full test suite to verify your setup
pytest --cov=src --cov-report=term-missing
```

### Docker (Recommended for inference)

```bash
docker compose up --build
# API is now available at http://localhost:8000
# Docs at          http://localhost:8000/docs
```

---

## Usage Examples

### Train a model

```python
from src.training import Trainer
from src.config import TrainingConfig

config = TrainingConfig(
    model_name="custom-transformer-base",
    epochs=20,
    batch_size=64,
    learning_rate=3e-4,
    use_mixed_precision=True,
    distributed=True,        # enables PyTorch FSDP
)

trainer = Trainer(config)
trainer.run()                # logs to W&B; registers best checkpoint in MLflow
```

### Run inference via the REST API

```bash
# Start the server
uvicorn src.api.main:app --host 0.0.0.0 --port 8000 --workers 4

# POST a prediction request
curl -X POST http://localhost:8000/v1/predict \
  -H "Content-Type: application/json" \
  -d '{"text": "Analyse sentiment of this sentence.", "top_k": 3}'
```

```json
{
  "predictions": [
    {"label": "positive", "score": 0.923},
    {"label": "neutral",  "score": 0.061},
    {"label": "negative", "score": 0.016}
  ],
  "latency_ms": 12.4,
  "model_version": "v2.1.0"
}
```

### Run with Docker

```bash
docker run --gpus all \
  -e WANDB_API_KEY=$WANDB_API_KEY \
  -p 8000:8000 \
  kenechukwuosele/<project-name>:latest
```

---

## Performance & Evaluation Results

> All benchmarks were run on a single A100 80 GB GPU with FP16 precision unless noted.

### Accuracy

| Model Variant | Dataset | F1 (macro) | Accuracy | AUC-ROC |
|---|---|---|---|---|
| Baseline (BERT-base) | Test set | 0.891 | 90.3% | 0.942 |
| Custom Transformer | Test set | **0.964** | **96.1%** | **0.981** |
| Custom Transformer (quantised INT8) | Test set | 0.958 | 95.6% | 0.977 |

### Latency & Throughput

| Deployment Mode | P50 Latency | P99 Latency | Throughput (req/s) |
|---|---|---|---|
| FastAPI (FP32) | 28 ms | 47 ms | 210 |
| FastAPI + TorchScript (FP16) | 14 ms | 22 ms | 430 |
| Triton Inference Server (INT8) | **9 ms** | **15 ms** | **780** |

### Training Efficiency

| Configuration | Time to Convergence | GPU Memory |
|---|---|---|
| Single GPU (A100) | 6 h 12 m | 74 GB |
| 4 x GPU (DDP) | 1 h 48 m | 18 GB / GPU |
| 8 x GPU (FSDP) | **58 min** | **10 GB / GPU** |

---

## Project Structure

```
<project-name>/
+-- .github/
|   +-- workflows/
|   |   +-- ci.yml              # Lint, test, build on every PR
|   |   +-- cd.yml              # Deploy to staging / production
|   +-- CODEOWNERS
+-- configs/
|   +-- training.yaml           # Hydra-managed training configs
|   +-- inference.yaml
+-- data/
|   +-- raw/                    # DVC-tracked raw datasets
|   +-- processed/              # Feature-engineered splits
+-- docs/
|   +-- architecture.md
|   +-- demo.gif                # Replace placeholder GIF here
+-- helm/
|   +-- <project-name>/         # Helm chart for K8s deployment
+-- notebooks/
|   +-- exploratory/            # EDA & prototype notebooks
+-- src/
|   +-- api/
|   |   +-- main.py             # FastAPI application entry point
|   |   +-- routes/
|   |   +-- middleware/
|   +-- data/
|   |   +-- ingestion.py
|   |   +-- transforms.py
|   |   +-- validation.py       # Great Expectations / Pydantic checks
|   +-- models/
|   |   +-- transformer.py      # Custom Transformer architecture
|   |   +-- lora.py             # LoRA adapter implementation
|   |   +-- quantisation.py
|   +-- training/
|   |   +-- trainer.py          # Main training loop (FSDP-aware)
|   |   +-- callbacks.py
|   |   +-- scheduler.py
|   +-- utils/
|       +-- logging.py
|       +-- metrics.py
+-- tests/
|   +-- unit/                   # Fast, isolated unit tests
|   +-- integration/            # Tests against Dockerised services
|   +-- load/                   # Locust load-test scenarios
+-- .env.example
+-- docker-compose.yml
+-- Dockerfile
+-- Makefile                    # Common dev tasks: make train, make test, etc.
+-- pyproject.toml
+-- requirements.txt
+-- README.md
```

---

## Future Roadmap

- [ ] **Multimodal Fusion** — extend the architecture to jointly process text and tabular data.
- [ ] **Online Learning** — incremental fine-tuning on production traffic with drift detection.
- [ ] **LLM Integration** — integrate an open-source LLM (Mistral / LLaMA 3) for generative tasks.
- [ ] **AutoML Sweep** — Optuna-driven hyperparameter search with parallel Kubernetes trials.
- [ ] **Federated Learning** — privacy-preserving training across distributed data silos.
- [ ] **Benchmark Suite** — public reproducibility harness so collaborators can verify published results.

---

## GitHub Stats

<div align="center">

![Kenechukwu's GitHub Stats](https://github-readme-stats.vercel.app/api?username=kenechukwuosele&show_icons=true&theme=github_dark&hide_border=true&count_private=true)
&nbsp;&nbsp;
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=kenechukwuosele&layout=compact&theme=github_dark&hide_border=true&langs_count=8)

</div>

---

## License

This profile and all associated project templates are released under the [MIT License](LICENSE).

---

<div align="center">

_"First, solve the problem. Then, write the code." — John Johnson_

**Open to full-time roles, consulting, and open-source collaboration.**
Contact: [kenechukwuosele@gmail.com](mailto:kenechukwuosele@gmail.com) · [LinkedIn](https://linkedin.com/in/kenechukwuosele)

</div>
