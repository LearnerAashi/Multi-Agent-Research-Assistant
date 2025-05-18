# Multi-Agent-Research-Assistant

## Overview

This project implements a **multi-agent AI system** capable of autonomously researching complex topics, synthesizing information, and generating comprehensive reports. The system demonstrates agentic behaviors like planning, reasoning, task decomposition, and collaboration — all orchestrated using Crewai.

### Research Query:
**"The business and technical implications of AI agents in enterprise settings"**

---

## Architecture

The system consists of the following components:

### Specialized Agents (via CrewAI)

1. **Researcher Agent**  
   - Conducts autonomous web searches
   - Gathers diverse, credible sources for the given topic

2. **Analyzer Agent**  
   - Synthesizes retrieved content
   - Extracts key business and technical insights

3. **Writer Agent**  
   - Structures the analyzed information into a coherent, citation-rich report

### CrewAI Coordination

- CrewAI enables seamless task delegation and conversation history sharing between agents.
- Agents operate within defined roles and interact via a shared memory and goal structure.

### API (FastAPI)

- `POST /submit-query` – Submit a new research query
- `GET /report/{query}` – Retrieve the generated report
- `GET /progress` – Monitor current agent activities

### Dockerized Deployment

- Fully containerized using Docker and Docker Compose
- Easily deployable on local or cloud environments

---

## Approaches to Solve the Assignment

### CrewAI-Based Solution (Implemented)
CrewAI simplifies agent-based orchestration with modular roles and task definitions. It enables:
- Reusable agent profiles
- Automatic role-based task routing
- Memory-sharing and inter-agent communication

### Alternative Architectures

#### 1. **LangGraph / LangChain Agents**
- Define agents with memory, tools, and a finite-state task graph.
- Use LangChain’s Tool abstraction for search, summarization, and writing.

#### 2. **AutoGen or MetaGPT**
- Use hierarchical agent stacks with controller/planner agents.
- Great for reasoning-intensive research tasks with recursive breakdowns.

#### 3. **Custom Python Multi-Agent Framework**
- Manually code each agent’s lifecycle and interactions.
- More flexible but increases complexity and boilerplate.

---



