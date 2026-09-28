<!-- ============================================================ -->
<!--                    SYNAPSE MAOS - README                     -->
<!-- ============================================================ -->

<div align="center">

<!-- LOGO (baad me apna logo daalna) -->
<!-- <img src="docs/diagrams/logo.png" alt="Synapse MAOS Logo" width="180"/> -->

# 🧠 Synapse MAOS

### Enterprise Multi-Agent Operating System

**Where AI Agents Connect, Collaborate & Conquer**

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18+-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org)
[![LangGraph](https://img.shields.io/badge/LangGraph-0.1+-FF6B6B?style=for-the-badge&logo=langchain&logoColor=white)](https://langchain.com)
[![Redis](https://img.shields.io/badge/Redis-7+-DC382D?style=for-the-badge&logo=redis&logoColor=white)](https://redis.io)
[![Neo4j](https://img.shields.io/badge/Neo4j-5+-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)](https://neo4j.com)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=for-the-badge)](CONTRIBUTING.md)

[Overview](#-overview) •
[Features](#-key-features) •
[Architecture](#-architecture) •
[Agents](#-the-six-agents) •
[Tech Stack](#-tech-stack) •
[Setup](#-quick-start) •
[API](#-api-reference) •
[Roadmap](#-roadmap)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Why Synapse MAOS?](#-why-synapse-maos)
- [The Six Agents](#-the-six-agents)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [System Flow](#-system-flow)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Quick Start](#-quick-start)
- [Environment Variables](#-environment-variables)
- [API Reference](#-api-reference)
- [Screenshots](#-screenshots)
- [Use Cases](#-use-cases)
- [Database Design](#-database-design)
- [Testing](#-testing)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)
- [Acknowledgments](#-acknowledgments)

---

## 🌟 Overview

**Synapse MAOS** (Multi-Agent Operating System) is a **distributed, agentic AI platform** that orchestrates **six specialized AI agents** to autonomously solve complex enterprise tasks. Instead of relying on a single monolithic LLM prompt, Synapse MAOS decomposes problems into subtasks, routes them to the right agent, validates outputs, optimizes results, and continuously monitors the entire pipeline — all in **real-time**.

> **Analogy:** Think of it as an **operating system for AI teams** — where each agent is a process, **Redis** is the IPC (inter-process communication) layer, **Neo4j** is the process dependency graph, **LangGraph** is the scheduler, and **Ray** is the distributed runtime.

### 🎯 The Core Idea

Traditional AI systems:



---

## 💡 Why Synapse MAOS?

| Problem with Single-Agent Systems | How Synapse MAOS Solves It |
|-----------------------------------|----------------------------|
| One agent does everything → poor quality | **Specialized agents** for each responsibility |
| No validation of output | **Auditor agent** validates every result |
| No continuous improvement | **Optimizer agent** refines outputs |
| No observability | **Observer agent** + Neo4j lineage tracking |
| Sequential & slow | **Ray-powered parallel execution** |
| No fault isolation | **Redis PubSub** decouples agents |
| Black-box behavior | **Full audit trail** in SQL + graph |

---

## 🎭 The Six Agents

<div align="center">

| Agent | Icon | Responsibility | Real-World Analogy |
|:-----:|:----:|----------------|:------------------:|
| **Planner** | 🧭 | Decomposes high-level tasks into atomic, ordered subtasks | Project Manager |
| **Coordinator** | 🎯 | Assigns subtasks to the right agent, manages dependencies | Team Lead |
| **Executor** | ⚡ | Performs actual task execution using tools & LLM reasoning | Engineer |
| **Auditor** | 🔍 | Validates outputs, flags inconsistencies, ensures quality | QA Engineer |
| **Optimizer** | 📈 | Improves efficiency, refines outputs, suggests better strategies | Process Expert |
| **Observer** | 👁️ | Monitors all agents, logs events, maintains system health | Supervisor |

</div>

### 🤝 Agent Collaboration Example

**Task**: *"Generate a Q4 sales report with insights and recommendations"*




---

## ✨ Key Features

### 🎯 Agentic Core
- ✅ **Autonomous task decomposition** — Planner breaks down any request
- ✅ **Intelligent routing** — Coordinator assigns work by capability
- ✅ **Parallel execution** — Ray distributes subtasks across CPU workers
- ✅ **Self-validation loop** — Auditor → Executor feedback cycle
- ✅ **Continuous optimization** — Optimizer refines every output
- ✅ **Full observability** — Observer tracks every agent event

### 🖥️ Frontend (React)
- 🎨 **Stunning dark-mode dashboard** with neon accents
- 📊 **Live agent activity feed** via WebSockets
- 🕸️ **Interactive workflow graph** (React Flow + Neo4j)
- 📈 **Real-time metrics & charts** (Recharts)
- 📜 **Comprehensive audit log viewer**
- 🎛️ **Task submission & control panel**
- 🔍 **Agent detail pages** with communication history
- 🌗 **Theme toggle** (dark/light)
- 📱 **Fully responsive** layout

### ⚙️ Backend (FastAPI)
- 🚀 **Async Python** (FastAPI + uvicorn)
- 🔌 **REST + WebSocket** APIs
- 🧠 **LangGraph state machine** workflow engine
- 📡 **Redis PubSub** message bus between agents
- 🕸️ **Neo4j** graph for task lineage
- 🗄️ **SQLAlchemy + SQLite** for persistence
- 🔐 **JWT authentication** ready
- 📝 **Structured logging** (loguru)
- ❤️ **Health checks** & metrics endpoints

### 🏢 Enterprise-Ready Patterns
- 🔄 Retry logic with exponential backoff
- 🎯 Agent-level rate limiting
- 📊 Prometheus-style metrics
- 🐳 Dockerized deployment
- 🧪 Pytest-based test suite
- 🛡️ Input validation with Pydantic v2
- 📖 OpenAPI/Swagger auto-docs

---

## 🏗️ Architecture

### High-Level Architecture



---

## 🛠️ Tech Stack

### 🔧 Backend

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Python** | 3.11+ | Core language |
| **FastAPI** | 0.110+ | REST API framework |
| **Uvicorn** | 0.27+ | ASGI server |
| **Pydantic** | v2 | Data validation |
| **SQLAlchemy** | 2.0+ | ORM |
| **Alembic** | 1.13+ | DB migrations |
| **LangGraph** | 0.1+ | Agent workflow engine |
| **LangChain** | 0.2+ | LLM abstractions |
| **CrewAI** | 0.30+ | Multi-agent collaboration |
| **Ray** | 2.10+ | Distributed execution |
| **Redis** | 7+ | PubSub + cache |
| **Neo4j** | 5+ | Graph database |
| **google-generativeai** | latest | Gemini SDK |
| **Loguru** | 0.7+ | Logging |
| **Pytest** | 8+ | Testing |
| **HTTPX** | 0.27+ | Async HTTP client |

### 🎨 Frontend

| Technology | Version | Purpose |
|-----------|---------|---------|
| **React** | 18+ | UI library |
| **Vite** | 5+ | Build tool |
| **TailwindCSS** | 3.4+ | Styling |
| **Framer Motion** | 11+ | Animations |
| **React Router** | v6 | Routing |
| **Zustand** | 4+ | State management |
| **Axios** | 1.6+ | HTTP client |
| **React Flow** | 12+ | Workflow graph viz |
| **Recharts** | 2.12+ | Charts |
| **Lucide React** | latest | Icons |
| **React Hot Toast** | 2+ | Notifications |
| **date-fns** | 3+ | Date utilities |

### 💾 Data Stores

| Store | Purpose |
|-------|---------|
| **SQLite / PostgreSQL** | Tasks, users, logs, audits |
| **Redis** | PubSub, cache, checkpoints |
| **Neo4j** | Agent graph, task lineage |

### 🚀 DevOps

- **Docker + Docker Compose**
- **Nginx** (reverse proxy)
- **GitHub Actions** (CI ready)

---

## 📁 Project Structure



---

## 🚀 Quick Start

### 📋 Prerequisites

| Tool | Version | Download |
|------|---------|----------|
| Python | 3.11+ | [python.org](https://python.org) |
| Node.js | 18+ | [nodejs.org](https://nodejs.org) |
| Redis | 7+ | [redis.io](https://redis.io) / [Memurai (Windows)](https://memurai.com) |
| Neo4j | 5+ | [neo4j.com/download](https://neo4j.com/download) |
| Git | latest | [git-scm.com](https://git-scm.com) |
| Gemini API Key | — | [aistudio.google.com](https://aistudio.google.com/app/apikey) |

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vishakha2121/Synapse---Enterprise-Multi-Agent-Operating-System.git
cd Synapse---Enterprise-Multi-Agent-Operating-System

cd backend

# Create virtual environment
python -m venv venv

# Activate
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Copy env template
copy .env.example .env    # Windows
cp .env.example .env      # macOS/Linux