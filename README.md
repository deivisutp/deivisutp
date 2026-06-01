<div align="center">
  <h1>Hi, I'm Deivis Utpadel</h1>
  <h3>Software Architect</h3>
  <p>Bridging the gap between legacy enterprise systems and modern AI agents.</p>
  
  <a href="https://www.linkedin.com/in/deivisutp" target="_blank">
    <img src="https://img.shields.io/badge/-LinkedIn-0e76a8?style=flat-square&logo=Linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:deivisutp@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/-Email-D14836?style=flat-square&logo=Gmail&logoColor=white" alt="Email">
  </a>
</div>

---

## About Me

With over 10 years of experience engineering and architecting scalable enterprise software, I specialize in the intersection of **Data Infrastructure, Backend Systems, and Artificial Intelligence**. My current focus is on building robust pipelines, developing **Model Context Protocol (MCP)** servers to give AI agents secure access to corporate data, and establishing rigorous LLM evaluation frameworks.

- **Currently building:** Advanced MCP servers for enterprise databases and terminal-based environments for AI evaluation.
- **Deep diving into:** LLM Fine-tuning, Reinforcement Learning from Human Feedback (RLHF), and Vector Databases.
- **Superpower:** Translating complex business rules into secure, scalable, and AI-ready architectures.
- **Location:** Brazil (UTC-3) — _Highly aligned with EST/PST workflows._

---

## Featured Projects & Architectural Case Studies

### 1. Enterprise Oracle MCP Server

[Link to Repository](https://github.com/deivisutp/oracle-mcp-server)

A production-grade **Model Context Protocol (MCP) server** that bridges AI assistants with large Oracle databases, solving the critical challenge of schema context at scale.

- **Core Problem Solved:** Enterprise Oracle databases can contain thousands of tables. Feeding an entire schema to an LLM is impractical. This server intelligently caches and serves schema information on demand, providing AI agents with only the context they actually need.
- **Architecture:** Built with `FastMCP` and `python-oracledb`, supporting dual transport modes — **stdio** for local desktop AI clients (GitHub Copilot, Claude) and **Streamable HTTP** for network-accessible deployments, with optional Bearer token authentication.
- **Key Features:** Smart schema caching, targeted table lookup, pattern-based table search, foreign key relationship mapping, and support for both thin and thick Oracle client modes.
- **AI Integration:** Works out-of-the-box with GitHub Copilot (VS Code), Claude Desktop, ChatGPT, and any MCP-compatible client — enabling natural language querying over complex relational schemas without manual context injection.
- **Stack:** `Python 3.11`, `FastMCP`, `python-oracledb`, `Docker`, `Oracle XE 21c`

### 2. Smart Financial Portfolio (with LLM Evaluation Layer)

A secure, single-tenant personal web application designed to consolidate investment portfolios and automate quarterly rebalancing.

Built with a **React/FastAPI** stack, this tool eliminates the need for complex spreadsheets by automatically ingesting trade data, applying daily fixed-income yields, and calculating the exact buy orders needed to hit your target asset allocation.

## Key Features

- **Automated Rebalancing:** Define your target allocation percentages. When making a new deposit, the system calculates the exact buy orders required to rebalance your portfolio—distributing funds to lagging assets without ever requiring you to sell.
- **B3 Statement Import:** Seamlessly upload B3 (Brazilian Stock Exchange) `.csv` or `.xlsx` statements. The engine supports both _Negotiation_ and _Movement_ layouts, automatically upserting Stocks, ETFs, FIIs, and Treasury bonds while calculating net balances and weighted average prices.
- **Fixed Income (CDI) Engine:** Register CDBs with their specific CDI percentage (e.g., 120% CDI). A daily background job fetches the official rate from the Central Bank of Brazil (Bacen API) and automatically applies compound interest.
- **Real-Time Quotes:** Fetches live market pricing for Brazilian equities via `yfinance` (automatically appending the `.SA` suffix to B3 tickers) whenever the dashboard is loaded.
- **Zero Trust Security:** Designed for secure self-hosting. Deployed via Docker Compose and Cloudflare Tunnels, meaning zero open inbound ports on the VPS and mandatory Identity Access Management (IAM) at the network edge.

## Tech Stack

- **Frontend:** React 18, Vite, Tailwind CSS (PWA ready)
- **Backend:** Python 3.11, FastAPI, SQLAlchemy
- **Database:** SQLite (Local persistent volume)
- **Infrastructure:** Docker Compose, Cloudflare Tunnels (Zero Trust)

A complete microservice architecture for financial tracking, engineered with a focus on modern MLOps principles and code evaluation.

- **Architecture:** FastAPI backend handling complex financial calculations, integrated with a React/Vite PWA, entirely orchestrated via Docker Compose and securely exposed via Cloudflare Tunnels.
- **AI Evaluation Showcase:** Includes a dedicated `/ai_evaluations` test suite where various LLMs were prompted to generate compound interest and rebalancing logic. Outputs were rigorously evaluated for edge cases, performance, and security vulnerabilities.
- **Stack:** `Python 3.11`, `FastAPI`, `SQLAlchemy`, `React 18`, `Docker Compose`, `LLM Prompting & Evaluation`

### 3. ImoFind API: Real Estate Data Engineering Pipeline

[Link to Repository](https://github.com/deivisutp/imofind-api)

An automated data extraction and structuring pipeline focused on capturing real estate market data in real-time.

- **Architecture:** Navigates complex DOM structures, handles data sanitization, and stores processed data in a relational database, exposing it via a documented REST API.
- **Why it matters:** Showcases strong foundational data engineering skills (ETL processes, web scraping, and data cleaning) required to build the datasets that power modern AI models.
- **Stack:** `Java 11`, `Spring Boot`, `JSOUP`, `Spring Data JPA`, `Swagger`

### 4. NutriPro – SaaS Platform for Nutrition Professionals

A comprehensive, cloud-based practice management platform built for nutritionists and nutrition clinics. NutriPro digitalizes and automates the entire operational workflow — from online appointment scheduling and patient evolution tracking to AI-powered diet suggestions and automated WhatsApp reminders.

**Live deployment:** [nutriprosolucoes](https://www.nutriprosolucoes.com.br/)

## Key Features

- **Appointment Scheduling** – Intuitive calendar-based booking system with automated confirmations
- **Patient Management** – Comprehensive patient profiles with evolution tracking and medical history
- **AI-Powered Diet Suggestions** – Leverages GPT-4o-mini to generate personalized diet plans
- **WhatsApp Integration** – Automated appointment reminders and patient communication via Twilio
- **Subscription Billing** – Stripe-powered recurring payments with multiple plan tiers
- **Admin Dashboard** – Real-time analytics, revenue tracking, and clinic management
- **LGPD Compliant** – Fully compliant with Brazilian data protection regulations
- **Live Chat Support** – Integrated Botpress chatbot for customer support
- **Responsive Design** – Mobile-first UI for practitioners on the go

## Technology Stack

| Layer                  | Technology                                          |
| ---------------------- | --------------------------------------------------- |
| **Frontend**           | Next.js 14 (App Router) + TypeScript + React 18     |
| **Styling**            | Tailwind CSS + shadcn/ui components                 |
| **Backend / Database** | Supabase (PostgreSQL) + Auth + RLS + Edge Functions |
| **Hosting**            | Vercel (serverless + cron jobs)                     |
| **Payments**           | Stripe (subscriptions + webhooks)                   |
| **AI Engine**          | OpenAI GPT-4o-mini                                  |
| **Chat Support**       | Botpress                                            |
| **PDF Generation**     | jsPDF                                               |

### 5. IGTI CI/CD Applied Project

A comprehensive full-stack application demonstrating modern CI/CD practices, microservices architecture, and DevOps methodologies.

[Link to Repository](https://github.com/deivisutp/igti-cicd-projeto-aplicado)

## Overview

This project showcases a production-ready Spring Boot backend with a React frontend, complete with automated testing, containerization, and cloud deployment infrastructure. It's designed as a capstone project combining software development best practices with continuous integration and deployment pipelines.

## Tech Stack

**Backend:**

- Spring Boot 2.4.3
- Spring Data JPA
- PostgreSQL
- Maven

**Frontend:**

- React.js
- JavaScript

**DevOps & Infrastructure:**

- Docker & Containerization
- Google Jib (Docker image building)
- AWS RDS (Relational Database Service)
- AWS Elastic Beanstalk
- GitHub Actions (CI/CD Pipeline)

**Testing & Quality:**

- Unit Testing
- Integration Testing
- Automated Code Review (ChatGPT integration)

**Monitoring:**

- Slack Integration for deployment notifications

## Key Features

- Full-stack web application with React frontend and Spring Boot REST API
- Containerized deployment using Docker and Jib
- Automated CI/CD pipeline with GitHub Actions
- Comprehensive testing suite (unit & integration tests)
- Cloud deployment on AWS (RDS + Elastic Beanstalk)
- Real-time deployment monitoring via Slack notifications
- Automated code review using ChatGPT language model
- Development and production environment configurations

### 6. Brasileirão API - Web Scraping Football Data Service

A Java Spring Boot REST API that automatically scrapes and aggregates Brazilian football league (Brasileirão) match data from Google in real-time.

[Link to Repository](https://github.com/deivisutp/brasileirao-api/)

## Overview

This project demonstrates modern web scraping techniques and backend development practices. The application automatically collects match information (teams, schedules, scores) from publicly available sources, processes the data, stores it in a relational database, and exposes it through a documented REST API.

## Key Features

- Automated Web Scraping: Uses JSOUP to parse and extract match data from Google search results
- Scheduled Tasks: Background jobs that run periodically to fetch and update match information
- REST API: Clean endpoints to retrieve teams (Equipe) and matches (Partida) data
- Real-time Data: Processes and serves the most current match information
- API Documentation: Interactive Swagger UI for easy API exploration and testing
- Robust Error Handling: Comprehensive exception management with custom error responses

## Technology Stack

Java 11+ with Spring Boot 2.4
Spring Data JPA for database operations
JSOUP for web scraping
H2 Database for lightweight data persistence
Swagger/Springfox for API documentation

## 7. Containerized Oracle Database Environment for Integration Testing

Overview:
A reusable CI/CD infrastructure component that provisions a fully-migrated Oracle XE 21c database (X tables) for automated integration testing of a system based on the defined schema. It is designed to be consumed as a shared GitHub Actions reusable workflow by multiple downstream projects.

[Link to Repository](https://github.com/deivisutp/dynamic-database)

Problem Solved:
Integration tests for Applications require a realistic Oracle database with proper schema, constraints, indexes, PL/SQL objects, and seed data. Setting this up manually is slow, error-prone, and inconsistent across developer machines and CI pipelines.

Architecture:

Docker Compose orchestration with two containers:

- Oracle XE 21c (gvenzl/oracle-xe:21-slim) - the database engine with health checks and resource limits.

- Alpine Migration Runner - a lightweight sidecar that waits for DB health, then executes ordered SQL migrations and PL/SQL deployments via docker exec.

- 6-phase migration pipeline: schema creation, table creation (1,044 tables), primary keys, foreign keys, indexes, and seed data.

- PL/SQL deployment: packages, functions, and procedures deployed separately via a dedicated script.

- Reusable GitHub Actions workflow that any project can reference to get a fully-provisioned test database without duplicating infrastructure code.

Key Technologies:
Oracle 21c, Docker Compose, Shell scripting, PL/SQL, GitHub Actions (reusable workflows), CI/CD pipeline design.

Highlights:

Extracted and reproduced a production-scale schemas into portable migration scripts.
Designed an idempotent, ordered migration system with error tolerance for seed data.
Enabled multiple development teams to run integration tests with a single workflow reference.
Supports project-specific custom migrations on top of the baseline.
Local developer experience: one docker-compose up -d command for a fully-provisioned database.

## 8. Dev Assistant Agent

Overview:
A conversational AI assistant that answers internal engineering questions grounded exclusively in a team's own documentation — not generic training data.

[Link to Repository](https://github.com/deivisutp/personal-agent)

What it does: Engineers query it in natural language ("How do I implement a new ComponentAction?") and receive precise, cited answers drawn directly from the codebase wiki, architecture docs, database models, and business rule documentation. 
Every response ends with a Sources section listing the exact internal documents used.

How it works:

Hybrid retrieval — Combines BM25 (keyword) and dense vector search (ChromaDB) fused via Reciprocal Rank Fusion, then optionally re-ranked by the LLM for maximum precision.

Smart ingestion — A markdown-structure-aware splitter preserves code fences, strips wiki noise ([[_TOC_]], HTML comments), and tags every chunk with rich metadata (doc_type, layer, language, heading_path) for filtered retrieval.

Flexible knowledge sources — Azure DevOps wikis, local folders, individual files, and raw text are all declared in a single knowledge_manifest.yaml, making the knowledge base easy to maintain and extend.

Persistent sessions — Chat history is stored in SQLite, enabling multi-turn conversations with full context continuity across restarts.

Web UI — HTMX-powered chat interface with real-time SSE streaming, syntax-highlighted code blocks, and a collapsible Sources panel under each answer.

Local-first — Runs entirely on-premise via Ollama. No data leaves the machine.

Stack: Python · FastAPI · LangChain · ChromaDB · BM25Okapi · Ollama · HTMX · SQLite

---

## Technical Arsenal

**AI & Data Engineering:** Python, Model Context Protocol (MCP), Web Scraping, Prompt Engineering, LLM Code Evaluation, SQLite, Oracle PL/SQL, Vector Concepts. <br>
**Backend & Architecture:** Java (Spring Boot, Hibernate), FastAPI, Node.js (NextJS), REST, Microservices, Event-Driven Architecture (RabbitMQ). <br>
**DevOps & Infrastructure:** Docker, Docker Compose, CI/CD Pipelines (GitHub Actions, Jenkins, AWS), Cloudflare Tunnels, Terminal Workflows. <br>
**Quality Assurance:** Test Automation (Playwright, TypeScript), SonarQube, Security Analysis (Fortify, BlackDuck).

---

<div align="center">
  <i>"Evaluating code critically — not only whether it works, but whether it is well-designed, secure, and maintainable."</i>
</div>
