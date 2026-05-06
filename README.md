<!-- MAHESH KOLLA — GitHub Profile README -->

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=venom&color=0:000000,30:050d1a,70:0a1628,100:0d1f3c&height=250&section=header&text=MAHESH%20%20KOLLA&fontSize=72&fontColor=f8fafc&animation=fadeIn&fontAlignY=45&desc=AI%20Engineer%20%E2%80%A2%20SAP%20Architect%20%E2%80%A2%20Enterprise%20Intelligence%20Builder&descAlignY=68&descSize=16&stroke=1d4ed8&strokeWidth=3"/>
</div>

<br>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=16&duration=2800&pause=900&color=60A5FA&center=true&vCenter=true&width=750&lines=_%20Building+AI+systems+that+run+in+production%2C+not+just+notebooks+_;_%20SAP+FI%2FCO+%2B+LLMs+%3D+a+combination+almost+nobody+has+_;_%20411+days.+59+weeks.+39+projects.+Zero+shortcuts+_;_%20Where+30-year-old+ERP+data+meets+cutting-edge+AI+_)](https://git.io/typing-svg)

</div>

<br>

---

<br>

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                             │
│   ██████╗ ██████╗  ██████╗ ███████╗██╗██╗     ███████╗                     │
│   ██╔══██╗██╔══██╗██╔═══██╗██╔════╝██║██║     ██╔════╝                     │
│   ██████╔╝██████╔╝██║   ██║█████╗  ██║██║     █████╗                       │
│   ██╔═══╝ ██╔══██╗██║   ██║██╔══╝  ██║██║     ██╔══╝                       │
│   ██║     ██║  ██║╚██████╔╝██║     ██║███████╗███████╗                     │
│   ╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝╚══════╝  v1.0.0-production │
│                                                                             │
│   STATUS:  🟢 ONLINE      LOCATION: Enterprise AI × SAP Finance            │
│   MISSION: Ship AI that finance teams actually use in production            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

<br>

## `$ whoami`

<table>
<tr>
<td width="60%" valign="top">

```yaml
identity:
  name: Mahesh Kolla
  title: AI Engineer + SAP S/4HANA Architect
  niche: "SAP Finance AI — the rarest stack in the market"

what_i_actually_do:
  - Build RAG systems that survive 10K concurrent users
  - Connect 30-year-old SAP data to cutting-edge LLMs
  - Ship ML models into FastAPI endpoints teams depend on
  - Design Azure pipelines: SAP → Snowflake → AI
  - Build multi-agent crews that replace manual workflows

philosophy: >
  Most people build AI demos.
  I build AI products.
  The difference shows in production logs.
```

</td>
<td width="40%" valign="top">

```
╔─────────────────────────╗
│   QUICK STATS           │
├─────────────────────────┤
│  📅  411  learning days │
│  📦   59  weeks built   │
│  🚀   39  live projects │
│  📚  151  resources used│
│  🏢   SAP  FI/CO expert │
│  🤖  LLM  RAG · Agents  │
│  ☁️  Cloud  AWS · Azure │
╚─────────────────────────╝
```

</td>
</tr>
</table>

<br>

---

## `$ cat superpower.txt`

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   The market has 50,000 AI engineers who know Python and LangChain.      ║
║                                                                          ║
║   The market has 30,000 SAP consultants who know FI/CO and S/4HANA.     ║
║                                                                          ║
║   The market has maybe 200 people who can fluently do BOTH               ║
║   and ship it to production.                                             ║
║                                                                          ║
║   ──────────────────────────────────────────────────────────────────     ║
║                                                                          ║
║   I am building to be in that 200.                                       ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

</div>

<br>

---

## `$ ls -la ./projects/`

<details>
<summary><code>🔶  sap-finance-llm-chatbot/</code> &nbsp;—&nbsp; <i>The flagship. SAP process Q&A + live Snowflake data via LLM</i></summary>

<br>

```
project/
├── rag_layer/        ← BGE-large embeddings over 200+ SAP T-code docs
├── sql_agent/        ← LangChain SQL agent over Snowflake dbt mart
├── router/           ← LangGraph: process_question vs data_question
├── guardrails/       ← NeMo rails + SQL injection whitelist
└── ui/               ← Streamlit with source citations + SQL display
```

**How it works:**
```
User: "Why was vendor 100234 blocked in FB60 last month?"
        │
        ▼
LangGraph Intent Router
   │                         │
   ▼                         ▼
RAG (process docs)       SQL Agent (Snowflake)
T-code guides            BKPF + BSEG live data
SAP posting rules        dbt mart views (GL/AP/AR)
   │                         │
   └───────────┬─────────────┘
               ▼
          Azure OpenAI GPT-4o
               ▼
    "Vendor 100234 was blocked due to..."
    [source: vendor_master.pdf, page 12]
```

| Metric | Value |
|--------|-------|
| Query latency | < 2 seconds |
| SQL injection blocks | 100% |
| Finance team adoption | 15 analysts |
| Lookup time reduction | 60% |

**Stack:** `LangGraph` `LangChain` `Azure OpenAI` `Chroma` `Snowflake` `NeMo Guardrails` `Streamlit`

</details>

<details>
<summary><code>🔶  sap-finance-ai-suite/</code> &nbsp;—&nbsp; <i>3 production ML models on SAP FI/AP data</i></summary>

<br>

```python
# Three models. One deployment. Real SAP data.

models = {
    "invoice_anomaly": {
        "algorithm":  "Isolation Forest + SHAP explanations",
        "data":       "BKPF + BSEG (10K+ postings)",
        "features":   ["amount_vs_vendor_avg", "weekend_posting_flag",
                       "duplicate_hash", "gl_account_mismatch"],
        "result":     "92% precision @ top-5% flagged",
    },
    "cash_flow_forecast": {
        "algorithm":  "Prophet + XGBoost ensemble",
        "data":       "Daily GL cash account (1100/1200) balances",
        "features":   ["payment_terms_lag", "posting_period_end",
                       "quarter_end_flag", "fiscal_year_day"],
        "result":     "8% MAPE on 30-day horizon",
    },
    "fraud_detector": {
        "algorithm":  "XGBoost + SMOTE (class imbalance handled)",
        "data":       "AP posting patterns + vendor behaviour",
        "features":   ["posting_time_anomaly", "amount_spike",
                       "new_vendor_flag", "duplicate_iban"],
        "result":     "F1 = 0.87 at optimal threshold",
    }
}
```

**Stack:** `scikit-learn` `Prophet` `XGBoost` `SHAP` `imbalanced-learn` `FastAPI` `Streamlit`

</details>

<details>
<summary><code>🔶  production-rag-pipeline/</code> &nbsp;—&nbsp; <i>Not a demo. Benchmarked, RAGAS-evaluated, CI-protected</i></summary>

<br>

```
NAIVE RAG (what everyone builds)        PRODUCTION RAG (what I built)
────────────────────────────────        ──────────────────────────────
Single vector search              →     BM25 + dense hybrid (RRF fusion)
No reranking                      →     Cross-encoder reranker (ms-marco)
Fixed chunk size                  →     Semantic + parent-child chunking
No evaluation                     →     RAGAS scorecard on every change
No CI                             →     Prompt regression CI in GitHub Actions
RAGAS faithfulness: 0.61          →     RAGAS faithfulness: 0.79  (+30%)
```

**Stack:** `LangChain` `FAISS` `Pinecone` `rank_bm25` `sentence-transformers` `RAGAS` `LangSmith`

</details>

<details>
<summary><code>🔶  azure-sap-ai-pipeline/</code> &nbsp;—&nbsp; <i>Enterprise SAP → Snowflake → AI, fully cloud-native</i></summary>

<br>

```
SAP S/4HANA
    │  OData extraction (delta load, BUDAT filter)
    ▼
Azure Data Factory ←── SAP Table Connector
    │  COPY INTO + Snowpipe auto-ingest
    ▼
Azure Synapse Analytics
    │  dbt: staging → intermediate → mart
    ▼
ML Feature Tables (vendor_behaviour, anomaly_inputs)
    │                         │
    ▼                         ▼
Azure AI Search           Feast Feature Store
(hybrid + semantic)       (Redis online, <10ms)
    │                         │
    └──────────┬──────────────┘
               ▼
        Azure OpenAI GPT-4o
        Azure Container Apps (FastAPI)
```

**Scale:** `500K+ invoices` · `<4h end-to-end` · `Managed Identity — zero hardcoded secrets`

</details>

<br>

---

## `$ cat ./tech_stack.json`

```json
{
  "ai_ml": {
    "frameworks":  ["PyTorch", "HuggingFace", "scikit-learn", "XGBoost", "Prophet"],
    "llm_stack":   ["LangChain", "LlamaIndex", "LangGraph", "CrewAI", "AutoGen"],
    "rag":         ["FAISS", "Pinecone", "Chroma", "Weaviate", "pgvector", "RAGAS"],
    "evaluation":  ["RAGAS", "LangSmith", "LLM-as-judge", "Evidently AI"]
  },
  "mlops": {
    "tracking":    ["MLflow", "Weights & Biases"],
    "pipelines":   ["Apache Airflow", "SageMaker Pipelines", "Vertex AI Pipelines"],
    "serving":     ["FastAPI", "Docker", "Kubernetes", "GitHub Actions"],
    "monitoring":  ["Evidently AI", "Prometheus", "Grafana"]
  },
  "cloud": {
    "azure":       ["ADF", "Synapse", "Azure OpenAI", "AI Search", "Azure ML", "Entra ID"],
    "aws":         ["SageMaker", "Lambda", "S3", "Bedrock", "ECR", "CloudWatch"]
  },
  "sap": {
    "modules":     ["FI", "CO", "S/4HANA", "BTP", "SAC", "Datasphere"],
    "extraction":  ["OData", "CDS Views", "BAPI", "ADF SAP Table Connector"]
  },
  "data": {
    "warehouse":   ["Snowflake", "Azure Synapse", "BigQuery"],
    "transform":   ["dbt", "PySpark", "Pandas"],
    "streaming":   ["Apache Kafka", "Faust"]
  }
}
```

<br>

---

## `$ ./progress --show-journey`

<div align="center">

```
AI ENGINEERING ROADMAP  ─────────────────────────────────  411 DAYS

PYTHON + TOOLS   ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  Python · OOP · DSA · Git
MATH FOR ML      ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  Linear Algebra · Stats · Calculus
MACHINE LEARNING ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  sklearn · XGBoost · SHAP
DEEP LEARNING    ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  PyTorch · CNN · Transformers
GENERATIVE AI    ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  LLMs · Prompting · Fine-tuning
RAG SYSTEMS      ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  Hybrid · Reranking · RAGAS
AI AGENTS        ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  LangGraph · CrewAI · AutoGen
MLOPS            ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  100%  Docker · CI/CD · Monitoring
DATA ENGINEERING ▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░   70%  Airflow · Kafka · dbt  ← NOW
SAP + AI         ▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░░░   60%  Chatbot · Finance AI   ← NOW
AZURE DEEP DIVE  ▓▓▓▓▓▓▓▓░░░░░░░░░░░░   40%  ADF · Synapse · OpenAI
SYSTEM DESIGN    ▓▓▓▓▓▓░░░░░░░░░░░░░░   30%  Scale · Microservices
DSA + INTERVIEWS ▓▓▓▓░░░░░░░░░░░░░░░░   20%  LeetCode · ML Design
```

</div>

<br>

---

## `$ git log --oneline --graph`

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=MAYA2k25&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=60a5fa&icon_color=60a5fa&text_color=e2e8f0&ring_color=1d4ed8&include_all_commits=true&count_private=true"/>
&nbsp;&nbsp;
<img height="170" src="https://github-readme-streak-stats.herokuapp.com/?user=MAYA2k25&theme=github-dark-blue&hide_border=true&background=0d1117&ring=1d4ed8&fire=60a5fa&currStreakLabel=e2e8f0&sideLabels=e2e8f0"/>

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=MAYA2k25&bg_color=0d1117&color=60a5fa&line=1d4ed8&point=60a5fa&area=true&area_color=1d4ed820&hide_border=true&custom_title=Contribution%20Graph%20—%20Building%20Every%20Day"/>

</div>

<br>

---

## `$ cat certifications.log`

```
[COMPLETED]   SAP S/4HANA Finance Certification
[COMPLETED]   DeepLearning.AI — LLM Specialization

[IN PROGRESS] ─────────────────────────────────────────────────────────
  → Microsoft Azure AI Engineer Associate (AI-102)
    Priority: HIGH — 80% of SAP enterprise shops run Azure
    ETA: Q2 2025

[QUEUED] ───────────────────────────────────────────────────────────────
  → AWS Certified Machine Learning Specialty
  → Google Professional ML Engineer
  → Snowflake SnowPro Core
```

<br>

---

## `$ ping connect`

<div align="center">

```
OPEN TO ROLES ─────────────────────────────────────────────────────────
  ✅  AI Engineer              — Finance / ERP domain
  ✅  LLM Engineer             — Enterprise AI products
  ✅  ML Engineer              — SAP + AI integration
  ✅  Senior AI Engineer       — Azure stack preferred
  ✅  SAP + AI Specialist      — Consulting or product
────────────────────────────────────────────────────────────────────────
  Location: Remote worldwide    Response time: < 24 hours
```

<br>

<a href="https://linkedin.com/in/YOUR-LINKEDIN">
<img src="https://img.shields.io/badge/LinkedIn-Let's%20Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
&nbsp;&nbsp;
<a href="mailto:YOUR-EMAIL@gmail.com">
<img src="https://img.shields.io/badge/Email-Reach%20Out-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</div>

<br>

---

<div align="center">

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   The best time to combine SAP expertise with AI engineering was         │
│   5 years ago.                                                           │
│                                                                          │
│   The second best time is right now.                                     │
│                                                                          │
│   That window won't stay open long.                                      │
│                                                                          │
│                                        — Building in public since 2024   │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,40:050d1a,100:1d4ed8&height=120&section=footer"/>

</div>
