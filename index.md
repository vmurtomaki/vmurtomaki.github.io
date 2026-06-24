---
layout: default
title: Portfolio | [Your Name]
description: Data Scientist specializing in advanced statistical modeling, MLOps, and agentic AI.
---

# [Your Name]

**Data Scientist &nbsp; &nbsp; M.Sc. Statistics &nbsp; &nbsp; Bridging Rigorous Inference & Scalable AI**

Welcome to my portfolio. I am a data scientist based in Finland, specializing in advanced statistical modeling, machine learning operations, and agentic AI. My work focuses on transforming complex, high-velocity data into production-ready architectures and actionable strategic insights.

| Category | Details |
| :--- | :--- |
| **Tech Stack** | Python, R, SQL, LangGraph, `llama.cpp`, Docker, MQTT, REST APIs |
| **Interests** | Spatial Econometrics, Maritime Logistics Optimization, Edge AI |

---

## Portfolio Projects

### 1. Spatio-Temporal Modeling of Regional Economic Vitality

* **Focus:** Bayesian Inference, Spatial Econometrics, Open Data Engineering
* **Tools:** R/Python, PXWEB API, INLA/Stan, GeoPandas

While many data scientists default to standard predictive modeling, this project highlights my foundation in mathematical statistics. Utilizing the PAAVO database from Statistics Finland (extracted programmatically via the PXWEB API), I engineered a spatial pipeline to analyze the endogenous demographic drivers and spatial spillover effects influencing disposable income across Finnish postal code areas (EUREF-FIN coordinate system).

To handle missing or censored public data thresholds robustly, I implemented a Bayesian Hierarchical Spatial Model (Besag-York-Mollie), accounting for adjacent postal code spatial contiguity. The underlying log-relative risk is modeled as:

$$\eta_i = \alpha + \mathbf{x}_i^\top \boldsymbol{\beta} + u_i + v_i$$

Where $\mathbf{x}_i$ represents local educational and workplace structures, $v_i \sim \mathcal{N}(0, \sigma_v^2)$ captures unstructured regional heterogeneity, and $u_i$ is the spatially structured Conditional Autoregressive (CAR) component defined as:

$$u_i | u_{-i} \sim \mathcal{N}\left( \frac{\sum_{j \sim i} w_{ij} u_j}{\sum_{j \sim i} w_{ij}}, \frac{\sigma_u^2}{\sum_{j \sim i} w_{ij}} \right)$$

**Key Outcomes:**

* Demonstrated programmatic extraction and cleaning of hierarchical government datasets.
* Showcased advanced handling of spatial contiguity matrices and spatio-temporal trends over a 14-year horizon.
* Delivered rigorous uncertainty quantification far beyond standard machine learning point estimates.

> **[View Repository / Read Case Study]** *(Link to be added)*

---

### 2. Real-Time Maritime Delay Prediction & MLOps Pipeline

* **Focus:** Streaming Data, MLOps, Gradient Boosting, Business Value Optimization
* **Tools:** Python, MQTT WebSockets, LightGBM/XGBoost, MLflow, Docker

Tailored to the maritime logistics hub of Southwest Finland, this project proves my ability to build predictive systems that generate immediate operational value. Instead of static CSVs, this architecture ingests live vessel location data via the Fintraffic Digitraffic MQTT WebSocket API, dynamically joining JSON payloads (course, heading, speed) with static ship metadata and sea state estimations.

The model forecasts Estimated Time of Arrival (ETA) deviations to classify the likelihood of significant port delays. Importantly, the model’s performance is evaluated not just on statistical error (RMSE), but on a custom cost-matrix that translates prediction errors into financial impacts—weighing the cost of prematurely preparing a berth versus the operational friction of a delayed arrival.

**Key Outcomes:**

* Engineered a robust streaming data ingestion pipeline for high-velocity telemetry.
* Packaged the trained Gradient Boosting model as a containerized RESTful API.
* Implemented experiment logging (MLflow) to demonstrate production readiness and model drift management.

> **[View Repository / Read Case Study]** *(Link to be added)*

---

### 3. Autonomous Data Engineering Agent on Constrained Hardware

* **Focus:** Agentic Workflows, LLM Quantization, Hardware Optimization
* **Tools:** LangGraph/Smolagents, Qwen 14B (IQ4_XS GGUF), Ollama

This project addresses the absolute frontier of generative AI: multi-step reasoning and autonomous tool usage deployed entirely locally. Operating under strict hardware constraints (Nvidia RTX 3060 12GB VRAM, 64GB System RAM), I optimized an agentic workflow using 4-bit quantization and strategic VRAM-to-System RAM offloading to maximize context window capabilities without sacrificing token generation speed.

Built using LangGraph, the AI acts as an autonomous junior data engineer. The agent is equipped with local tools to scrape endpoint documentation from `opendata.fi`, write data parsing scripts in Python, and execute them in a sandboxed environment. If an execution throws a traceback error, the agent autonomously reads the stack trace, self-corrects the code, and loops until the dataset is successfully compiled and saved.

**Key Outcomes:**

* Proved deep understanding of LLM memory constraints, Key-Value cache management, and hardware-level quantization (GGUF).
* Built a stateful, cyclic AI orchestration graph capable of self-healing code execution.
* Delivered a locally hosted, privacy-preserving alternative to expensive, cloud-based agentic frameworks.

> **[View Repository / Read Case Study]** *(Link to be added)*

---

### Let's Connect

I am currently seeking Data Scientist and Machine Learning Engineering roles in Finland. Let's discuss how my background in statistics and software engineering can drive value for your team.

* **Email:** [your.email@example.com]
* **LinkedIn:** [Your LinkedIn Profile]
* **GitHub:** [Your GitHub Profile]
