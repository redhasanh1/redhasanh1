# Hasan Iqbal

I build AI, ML, and full-stack systems — currently focused on inference performance, computer vision pipelines, and production AI. Open to internships and full-time roles.

[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Swift](https://img.shields.io/badge/Swift-FA7343?logo=swift&logoColor=white)](https://www.swift.org/)
[![Java](https://img.shields.io/badge/Java-007396?logo=openjdk&logoColor=white)](https://www.java.com/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![TensorRT](https://img.shields.io/badge/TensorRT-76B900?logo=nvidia&logoColor=white)](https://developer.nvidia.com/tensorrt)
[![CUDA](https://img.shields.io/badge/CUDA-76B900?logo=nvidia&logoColor=white)](https://developer.nvidia.com/cuda-toolkit)
[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white)](https://supabase.com/)

---

## Selected work, at a glance

| | |
|---|---|
| **35×** | inference speedup on a 19B-parameter video diffusion model (RTX 5090) |
| **YOLOv8** | custom detector trained on 1,000+ annotated frames, deployed via TensorRT |
| **48** | transformer attention layers replaced with custom TensorRT engines |
| **1,247** | negotiations analyzed in a closed-loop learning system |
| **Web + iOS + Android** | one full-stack AI rental marketplace, all three sharing a single API |
| **9 waves** | of optimization experiments — successes and failures both publicly documented |

---

## Featured projects

### [RoomFinderAI](https://github.com/redhasanh1/RoomFinderAI)

**An AI-powered rental marketplace that replies to inquiries in under 60 seconds, shows you the real monthly cost of a place instead of just the rent, and helps you negotiate with landlords using patterns learned from 1,247 past conversations.**

- Full-stack across **web (vanilla JS), iOS (SwiftUI), and Android (Java)** — all sharing a Node/Express + Supabase backend.
- Closed-loop learning system over 22 response templates with epsilon-greedy selection (top template: 82% win rate over 45 samples).
- Vision AI pricing model on **Cloudflare Workers AI (Llama 3.2 11B Vision)** — luxury score, money-feature extraction, suggested rent.
- 15+ external data feeds (RentCast, Walk Score, GreatSchools, FBI Crime, FEMA, NOAA, EPA, BLS, USGS, Google Distance Matrix) joined into per-listing market intelligence.
- 60+ REST endpoints, 27 SQL migrations with row-level security, real-time chat via Supabase Realtime, Stripe payments, Azure ID verification.

### [Video-Generator](https://github.com/redhasanh1/Video-Generator)

**Text-to-video inference performance project — took a 19B-parameter diffusion transformer from 295 seconds per clip to 8.4 seconds on a single RTX 5090.**

- **35× end-to-end speedup** across 9 documented "waves" of optimization. Every wave has a benchmark verdict; the failures got post-mortems too.
- **TensorRT attention engines** for all 48 transformer attention layers, lazy-loaded to avoid OOM (`TRTAttentionPatcher`).
- **FP8 GEMM** on Blackwell tensor cores, **SageAttention3** with FP4 quantization, **TeaCache** at 0.10 threshold, **torch.compile** with max-autotune and graph-break elimination.
- Documented failure post-mortems for 9 abandoned experiments — TGATE caching, DeepCache, AdaCache, 2:4 sparsity, K/V precomputation, and more — each with a written root cause.
- Built on top of Lightricks' LTX-2 foundation model. The optimization work and tooling are mine.

### [Neural-Video-Inpainting](https://github.com/redhasanh1/Neural-Video-Inpainting)

**Production-grade video object-removal pipeline. Detects, tracks, and reconstructs target regions across temporal sequences — built for distributed GPU cloud deployment.**

- Multi-model architecture: **YOLOv8** (custom-trained on 1,000+ annotated frames) → **SAM2** mask propagation → **ProPainter** temporal inpainting.
- ProPainter stack uses **RAFT optical flow**, **Focal Transformer attention**, and **DCNv4 deformable convolutions** — including custom DCNv4 CUDA kernels.
- TensorRT FP16/FP8 quantization end-to-end, GPU-accelerated NVDEC/NVENC preprocessing, FFmpeg reassembly with audio merge.
- Designed for horizontal scaling across distributed GPU workers.

---

## Smaller projects worth a look

- **[Olympics Athlete Data Analysis](https://github.com/redhasanh1/RoomFinderAI/tree/main/data%20stufff/project-g4-hiqbal7-slmason-sthakkar11-eshahnaghi-main)** — Group project (4 people). Python data-cleaning pipeline over the Olympic Games datasets: schema validation, malformed-date repair, missing-value strategies, duplicate detection across athlete records. Light, but it's where I first started thinking carefully about data quality before touching production data systems.

---

## Earlier work

A timeline of where I was learning. Not flagship work — left here because portfolios should show the slope, not just the peak.

- **[SheridanCapstoneApp-Staging3](https://github.com/redhasanh1/SheridanCapstoneApp-Staging3)** — React Native mobile app for a Computer Engineering Technology capstone (TypeScript, 2023).
- **[CaseStudy1_1](https://github.com/redhasanh1/CaseStudy1_1)** — Kotlin Android case study (2023).
- **[Website](https://github.com/redhasanh1/Website)** — Call of Duty stats / records site (2024).
- **[ActualProject2](https://github.com/redhasanh1/ActualProject2)**, **[case](https://github.com/redhasanh1/case)**, **[new](https://github.com/redhasanh1/new)** — early exploration / learning repos (2022–2023).

---

## What I work with

| Languages | ML, vision, GPU | Backend, mobile, cloud |
|---|---|---|
| Python, JavaScript, TypeScript | PyTorch, TensorRT, ONNX | Node.js + Express |
| Swift, Java, Kotlin | CUDA, FP8 / FP4 quantization | Supabase (Postgres + Realtime + Auth) |
| SQL, HTML/CSS | torch.compile, SageAttention3 | SwiftUI (iOS), Java + Material 3 (Android) |
| Bash, PowerShell | YOLOv8, SAM2, ProPainter | Cloudflare Workers AI, Stripe, Azure (Document Intelligence + Face) |
|  | OpenAI / LLM prompt engineering | Docker, Railway, Git |

---

## GitHub

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=redhasanh1&show_icons=true&hide_border=true&theme=tokyonight&count_private=true)](https://github.com/redhasanh1)
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=redhasanh1&layout=compact&hide_border=true&theme=tokyonight&langs_count=8)](https://github.com/redhasanh1)

---

**Hasan Iqbal** — [github.com/redhasanh1](https://github.com/redhasanh1) — hasaniqbal2@hotmail.com
