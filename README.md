# 📄 Doc-Intelligence-Core

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-brightgreen.svg)](https://www.python.org/downloads/)
[![Multi-Modal-AI](https://img.shields.io/badge/Focus-Multi--Modal--AI-orange.svg)]()
[![Document-Intelligence](https://img.shields.io/badge/Field-IDP-red.svg)]()

**Doc-Intelligence-Core** is an advanced Multi-Modal framework designed for **Intelligent Document Processing (IDP)**. It leverages Vision-LLMs and Layout-aware agents to autonomously understand complex document structures, perform precise layout analysis, and extract verified data from unstructured sources (PDFs, scans, and forms).

---

## 🚀 Key Features

- **🎯 Autonomous Layout Analysis:** High-precision detection of document elements (tables, headers, footers) using multi-modal perception.
- **🔄 Verification-First Extraction:** Integrated feedback loops to cross-verify extracted data against symbolic rules and document context.
- **📊 Complex Table Parsing:** Specialized logic for deconstructing high-density tabular data, built on patent-pending extraction principles.
- **🧠 Cognitive Document Agents:** Agents that can reason about document "intent" rather than just performing simple OCR.
- **🔌 Schema-Aware Output:** Automatically maps extracted data to structured JSON/Pydantic schemas for downstream enterprise consumption.

---

## 🏗️ Architecture

`mermaid
graph LR
    A[Raw Document / Image] --> B[Multi-Modal Perception]
    B --> C[Layout Analyzer Agent]
    C --> D[Visual Element Extraction]
    D --> E{Verification Engine}
    E -- Validated --> F[Structured Data / JSON]
    E -- Error --> G[Human-in-the-Loop / Re-analysis]
    F --> H[Enterprise Downstream]
`

---

## 🛠️ Project Structure

`	ext
Doc-Intelligence-Core/
├── src/
│   ├── agents/         # Layout analysis and extraction agents
│   ├── perception/     # Vision-LLM and OCR integration
│   ├── extraction/     # Tabular and text parsing logic
│   └── verification/   # Data validation and consistency checks
├── tests/              # End-to-end extraction benchmarks
└── requirements.txt    # Project dependencies
`

---

## 📖 Quick Start

`python
from src.agents.layout_analyzer import VisualLayoutAnalyzer

# 1. Initialize the Analyzer
analyzer = VisualLayoutAnalyzer()

# 2. Process a document
image_path = "path/to/invoice.png"
structure = analyzer.analyze_layout(image_path)

# 3. Inspect detected elements
for element in structure.elements:
    print(f"Detected {element.label} with {structure.confidence_score*100}% confidence")
`

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
<p align="center">Crafted with ❤️ by <a href="https://github.com/Salset0">Harinath Krishnamoorthy</a></p>