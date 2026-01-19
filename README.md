# LLM-Driven Framework for Antibiotic Resistance Gene (ARG) Detection

## Thesis Diagrams Repository

> **Final Year Design Project (FYDP) — January 2026**  
> System architecture and design diagrams for thesis documentation.

**Note:** This repository contains only the **design diagrams** for the LLM-Driven ARG Framework thesis. The source code and implementation are maintained in a separate repository.

---

## Project Overview

This repository contains the **system architecture diagrams and design documentation** for an LLM-driven framework designed to identify and validate Antibiotic Resistance Genes (ARGs) from genomic sequences. The framework integrates traditional sequence alignment tools with modern AI reasoning capabilities to provide researchers with explainable, context-rich analysis results.

### Problem Statement

Traditional ARG detection methods rely solely on sequence similarity, often producing:
- High false-positive rates
- Limited contextual understanding
- No explanation of resistance mechanisms
- Difficulty interpreting edge cases

### Proposed Solution

Our framework augments bioinformatics pipelines with:
- **Retrieval-Augmented Generation (RAG)** for contextual enrichment
- **LLM-based reasoning** for validation and explanation
- **Structured reporting** with natural language interpretations

---

## System Architecture

The framework consists of three primary layers:

### 1. Client Layer
- **Web User Interface**: FASTA file upload, real-time progress tracking, interactive results table, and detailed explanation panel

### 2. Application / Backend Layer
| Module | Description |
|--------|-------------|
| **Backend Controller** | Orchestrates the pipeline workflow (Python) |
| **Sequence Alignment** | DIAMOND/BLAST-based homology search |
| **RAG / CARD Retrieval** | ARO lookup for resistance metadata |
| **Prompt Engineering** | Combines alignment results with ontological context |
| **LLM Reasoning Engine** | Sends structured prompts to LLM API |
| **Report Generation** | Produces JSON + natural language reports |

### 3. External Systems
- **CARD Database**: Comprehensive Antibiotic Resistance Database (ontology & metadata)
- **LLM Provider API**: Cloud-based reasoning and validation service

---

## Diagrams Included

This repository contains the following thesis-ready diagrams in `diagrams.html`:

| Figure | Title | Description |
|--------|-------|-------------|
| **3.1** | Context Diagram | High-level system boundaries showing User, CARD Database, and LLM Provider interactions |
| **3.2** | Data Flow Diagram (Level 1) | Detailed DFD showing 5 core processes with data stores and flows |
| **3.3** | User Interface Wireframe | Mockup of the web application interface |
| **3.4** | Project Plan (Gantt Chart) | Development timeline and milestones |
| **3.5** | System Architecture Diagram | Comprehensive multi-layer architecture view |

---

## Data Flow Pipeline

```
┌──────────────┐    FASTA File    ┌─────────────────────┐
│     User     │ ───────────────► │  1.0 Sequence       │
│ (Researcher) │                  │      Alignment      │
└──────────────┘                  └─────────┬───────────┘
       ▲                                    │
       │                           Candidate Hits
       │                                    ▼
       │                          ┌─────────────────────┐
       │                          │  2.0 Context        │◄────► CARD Database
       │                          │      Retrieval      │
       │                          └─────────┬───────────┘
       │                                    │
       │                           Enriched Context
       │                                    ▼
       │                          ┌─────────────────────┐
       │                          │  3.0 Prompt         │
       │                          │      Engineering    │
       │                          └─────────┬───────────┘
       │                                    │
       │                           Formatted Prompt
       │                                    ▼
       │                          ┌─────────────────────┐
       │                          │  4.0 LLM            │◄────► LLM Provider
       │                          │      Reasoning      │
       │                          └─────────┬───────────┘
       │                                    │
       │                           Validation Result
       │                                    ▼
       │                          ┌─────────────────────┐
       │    Analysis Report       │  5.0 Report         │
       └────────────────────────── │      Generation     │
                                  └─────────────────────┘
```

---

## Technologies & Tools

| Category | Technologies |
|----------|--------------|
| **Backend** | Python |
| **Sequence Alignment** | DIAMOND, BLAST |
| **Knowledge Base** | CARD (Comprehensive Antibiotic Resistance Database) |
| **AI/ML** | Large Language Models (via API) |
| **Data Format** | FASTA, JSON |
| **Documentation** | HTML/SVG (thesis diagrams) |

---

## Repository Structure

```
Diagram/
├── README.md              # This file
├── diagrams.html          # All thesis diagrams (Figures 3.1–3.5)
└── diagram.txt            # Working notes (excluded from git)
```

---

## Key Features

- **Explainable AI**: LLM provides natural language reasoning for each ARG prediction
- **Context-Aware Validation**: RAG enriches results with CARD ontology metadata
- **End-to-End Pipeline**: From FASTA upload to structured analysis report
- **Professional Reporting**: JSON for programmatic access, NL for human interpretation
- **Modular Architecture**: Each component can be independently updated or replaced

---

## Academic Context

This project is submitted as part of an undergraduate **Final Year Design Project (FYDP)** in the field of computational biology and artificial intelligence. The diagrams follow standard software engineering notation:

- **Context Diagram**: DFD Level 0 notation
- **Data Flow Diagram**: Gane-Sarson DFD notation (processes as circles, data stores as open rectangles)
- **System Architecture**: Layered architecture representation

---

## Viewing the Diagrams

Open `diagrams.html` in any modern web browser to view all diagrams:

```bash
# Using default browser
xdg-open diagrams.html        # Linux
open diagrams.html            # macOS
start diagrams.html           # Windows
```

The diagrams are rendered as inline SVG graphics and are optimized for:
- Screen viewing
- Print (A4/Letter)
- PDF export
- Thesis document embedding

---

## Author

**Final Year Design Project**  
*LLM-Driven Framework for ARG Detection*  
January 2026

---

This project is developed for academic purposes. All diagrams and documentation are original work created for thesis submission.

---

<p align="center">
  <i>Professional Academic Documentation for Thesis Submission</i>
</p>