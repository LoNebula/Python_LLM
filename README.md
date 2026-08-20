<p align="center">
  <img src="assets/hero.svg" alt="⚡ PyTorch & Ollama GPU Deep Learning Stack Hero Banner" width="100%" />
</p>

<h1 align="center">⚡ PyTorch & Ollama GPU Deep Learning Stack</h1>

<p align="center">
  <strong>Reproducible, isolated NVIDIA GPU-accelerated Docker Compose environment combining PyTorch development with local Ollama LLM inference.</strong>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-license">License</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Compose v2-2496ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" /> <img src="https://img.shields.io/badge/NVIDIA_CUDA-12.x-76b900?style=for-the-badge&logo=nvidia&logoColor=white" alt="NVIDIA_CUDA" /> <img src="https://img.shields.io/badge/PyTorch-2.0+-ee4c2c?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" /> <img src="https://img.shields.io/badge/Ollama-Local LLM-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" />
</p>

---

## ✨ Features (Key Outcomes & Capabilities)

| Icon | Feature | Outcome & Real Proof |
| :---: | :--- | :--- |
| 🚀 | **GPU-Accelerated Container Stack** | Full NVIDIA Container Toolkit pass-through for high-throughput CUDA compute |
| 🦙 | **Integrated Ollama LLM Service** | Persistent local LLM server ready to serve Llama 3, Qwen, DeepSeek, and Mistral models |
| 📓 | **JupyterLab & Python Workspace** | Pre-configured data science environment with PyTorch, Transformers, and Accelerate |
| 🛡️ | **Host-Isolated Reproducibility** | Clean architecture that prevents host environment pollution and dependency conflicts |

---

## 📊 Architecture & Flow

```mermaid
graph TD
  Host[🖥️ Host OS + NVIDIA GPU Drivers] --> Docker[🐳 Docker Compose Stack]
  Docker --> Container1[⚡ PyTorch Development Container & JupyterLab]
  Docker --> Container2[🦙 Ollama Local LLM Inference Container]
  Container1 <-->|HTTP API :11434| Container2
  
  classDef primary fill:#10b981,stroke:#059669,stroke-width:2px,color:#fff;
  classDef accent fill:#6366f1,stroke:#4f46e5,stroke-width:2px,color:#fff;
  class Docker primary;
  class Container1,Container2 accent;
```

---

## 📁 Project Structure

```bash
python_llm/
├── 📄 docker-compose.yml      # Multi-container GPU stack definition
├── 📄 Dockerfile              # PyTorch + CUDA base image
├── 📄 Python_llm.ipynb        # Example LLM inference & fine-tuning notebook
└── 📄 README.md               # Stack documentation
```

---

## 🚀 Quick Start

### Prerequisites
- Check language runtimes (Python / Node.js) and system dependencies.

```bash
# 1. Start all GPU services
docker compose up -d

# 2. Open JupyterLab: http://localhost:8888
# 3. Pull an Ollama model:
docker compose exec ollama ollama pull llama3
```

---

## 💡 Usage Notes & Tips

> [!TIP]
> Ensure all required environment variables and dependencies are properly configured before execution.

---

<p align="center">
  Released under the <a href="LICENSE">MIT License</a>. Made with ❤️ by <a href="https://github.com/LoNebula">LoNebula</a>
</p>
