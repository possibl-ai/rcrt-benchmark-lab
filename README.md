# RCRT Benchmark Lab

Live benchmark showcase dashboard for RCRT. Fetches real-time data from the RCRT Benchmark API and visualizes how RCRT's intelligent context engine outperforms traditional retrieval approaches.

## What it shows

- **KPI Summary**: Best/average RCRT accuracy, win rate, cost savings
- **Accuracy Comparison**: Grouped bar chart comparing RCRT vs baselines per benchmark
- **Cost Efficiency**: Cost per correct answer across surfaces
- **Deep Dive by Category**: Detailed accuracy breakdown with explanations of what each question category tests (direct retrieval, multi-hop reasoning, cross-scope, archival, override)
- **Run Details**: Expandable cards with head-to-head task results

## Surface Labels

The dashboard shows the actual technology stack, not abstract names:

- `rcrt_full` → **RCRT + Haiku 4.5** (full RCRT platform with LOD context engine)
- `traditional_rag` → **Vertex AI Search + Sonnet 4.6** (same search, flat top-K retrieval)
- `plain_model` → **Opus 4.6 Direct** (no retrieval at all)

## Running locally

```bash
# Just open index.html in a browser - it's self-contained
open index.html
```

## Deploy to Cloud Run

```bash
gcloud builds submit --config=cloudbuild.yaml --project=rcrt-v3-dev
```

## Preview Service

Works with the RCRT preview service:
```
https://rcrt-preview-service-1038267090431.us-central1.run.app/#owner=possibl-ai&repo=rcrt-benchmark-lab
```
