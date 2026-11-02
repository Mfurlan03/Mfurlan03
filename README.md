# Hey, I'm Michael 👋

ML engineer with an Industrial Engineering background (University of Toronto, Class of 2026).
I build ML systems where the hard part isn't fitting a model but knowing whether to trust it:
evaluation harnesses, leakage checks, honest baselines, and the engineering around them
(APIs, tests, CI, containers).

- 🔍 Retrieval-augmented generation, evaluation design, small-data and imbalanced problems, time series
- 🧪 I measure before I claim: every project below ships with a reproducible evaluation, and several of them caught real bugs that way
- 💼 Open to **ML / AI engineering** roles
- 📍 Toronto (Eastern Time) · [LinkedIn](https://linkedin.com/in/michaelfurlano) · furlanomichael02@gmail.com

---

## Featured projects

### 🤖 [discord-rag-backend](https://github.com/Mfurlan03/discord-rag-backend): RAG FAQ bot with a retrieval eval harness
FastAPI service + Discord bot that answers questions from a document base with cited sources.
Pluggable retrieval (MongoDB Atlas Vector Search, or in-memory **dense / BM25 / hybrid RRF**),
any OpenAI-compatible LLM, and a **36-question labeled eval** (Hit@k, MRR) that compares
chunking strategies and retrievers. Graceful degradation, no-secret config endpoint,
31 offline tests via dependency injection, Docker + CI.
<br>`Python` `FastAPI` `sentence-transformers` `MongoDB Atlas` `Docker` `GitHub Actions`

### 📉 [metricguard](https://github.com/Mfurlan03/metricguard): detecting KPI gaming (Goodhart's Law) in time series
Python package and CLI that flags when a KPI decouples from the outcome it's supposed to track,
using interpretable, noise-scaled signals. Ships a **labeled detection benchmark** (ROC-AUC,
false-positive rate, window IoU) with constants calibrated on held-out seeds. The benchmark
exposed a scale bug that flagged 100% of clean series; the fix took ROC-AUC from 0.49 to 1.00
on that scenario.
<br>`Python` `pandas` `NumPy` `pytest` `GitHub Actions`

### 🎵 [multi-output-audio-regression](https://github.com/Mfurlan03/multi-output-audio-regression): predicting 11 music attributes from raw audio
librosa feature pipeline → per-target Random Forest and a GRU over frame sequences. Showed
that raw averaged MSE was 97% tempo and hid everything else, and moved evaluation to
per-target R² against a mean baseline. A synthetic sanity dataset revealed that a joint
multi-output forest lets noisy targets hijack shared splits.
<br>`Python` `PyTorch` `librosa` `scikit-learn`

### 🏀 [nba-draft-success](https://github.com/Mfurlan03/nba-draft-success): career-tier prediction from pre-draft data
Team project. Scraped and merged college, combine and NBA data; built a leakage-guarded
pipeline with repeated CV, ordinal metrics (quadratic-weighted kappa) and a label-permutation
test. The honest result: on 109 matched players no model beats chance significantly
(p = 0.27), and the bottleneck is data matching, not model choice.
<br>`Python` `scikit-learn` `pandas`

### 💻 [campustech-connect](https://github.com/Mfurlan03/campustech-connect): student laptop marketplace
Team project: Spring Boot REST API with JWT auth, buyer/seller roles, wishlists with price
alerts, program-based recommendations and external price comparison.
<br>`Java 17` `Spring Boot` `Spring Security` `Swagger`

---

## Skills

- **ML / AI:** PyTorch, scikit-learn, sentence-transformers, RAG (vector, BM25, hybrid retrieval), evaluation design
- **Engineering:** Python, FastAPI, Docker, GitHub Actions, pytest, Git, SQL, MongoDB
- **Data:** pandas, NumPy, Matplotlib, Tableau, Power BI
- **Also used:** Java, C++, R, MATLAB, JavaScript

---

If you're working on a problem where getting the evaluation right matters, I'd love to talk.
