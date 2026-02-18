# 🧠 Google Gemini API – Models, Pricing & Free Tier Guide

A practical reference for choosing the **right Gemini model** for your use case:  
**code assistants, chatbots, image generation, and embeddings**.

Source: https://ai.google.dev/gemini-api/docs/models.md.txt

---

## 📌 Quick “Which Model Should I Use?”

| Use Case | Recommended Model |
|--------|------------------|
| Code assistant / reasoning | `gemini-2.5-pro` |
| Production chatbot | `gemini-2.5-flash` |
| High-scale low-cost chatbot | `gemini-2.5-flash-lite` |
| Low-latency assistant | `gemini-3-flash-preview` |
| Image generation | `gemini-2.5-flash-image` |
| Semantic search / RAG | `gemini-embedding-001` |

---

## 🆓 Free Tier & Rate Limits (Overview)

Google Gemini API provides a **free tier** (no credit card required) for testing and prototyping.

### Free Tier Characteristics
- Limited **Requests Per Minute (RPM)**
- Limited **Tokens Per Minute (TPM)**
- Daily request caps
- Shared quota across models

> ⚠️ Exact limits vary by model and may change.  
> Always check **Google AI Studio → Quotas** for real values.

### Typical Free Tier Limits (Indicative)

| Metric | Free Tier |
|-----|----------|
| Requests per minute | ~5–15 RPM |
| Tokens per minute | ~250,000 TPM |
| Daily requests | Limited |
| Production SLA | ❌ No |

### Paid Tier Benefits
- Much higher RPM / TPM
- Stable production throughput
- Billing-based scaling
- Required for serious production workloads

---

## 📊 Gemini API Models – Full Reference Table

| API Model ID | Display Name | Description | Primary Use Cases | Free Tier | Paid Pricing (per 1M tokens) |
|-------------|-------------|-------------|------------------|----------|------------------------------|
| `gemini-3-pro-preview` | Gemini 3 Pro (Preview) | Most powerful multimodal reasoning model | Deep reasoning, large context analysis, research | Limited | Input $2–$4 / Output $12–$18 |
| `gemini-3-flash-preview` | Gemini 3 Flash (Preview) | Low-latency, fast multimodal model | Real-time chat, agents | ✅ Yes | Input $0.50 / Output $3.00 |
| `gemini-3-pro-image-preview` | Gemini 3 Pro Image | Image generation & multimodal | High-quality image generation | Limited | Text $2 / Image priced separately |
| `gemini-2.5-pro` | Gemini 2.5 Pro | High-end reasoning & coding model (1M context) | Code assistants, logic, analysis | ✅ Yes | Input $1.25–$2.50 / Output $10–$15 |
| `gemini-2.5-flash` | Gemini 2.5 Flash | Balanced cost & performance | Chatbots, assistants, workflows | ✅ Yes | Input ~$0.30 / Output ~$2.50 |
| `gemini-2.5-flash-image` | Gemini 2.5 Flash Image | Text-to-image generation | Image generation apps | Limited | Flash pricing + image tokens |
| `gemini-2.5-flash-lite` | Gemini 2.5 Flash-Lite | Ultra-low cost, high throughput | Large-scale bots | ✅ Yes | Input $0.10 / Output $0.40 |
| `gemini-embedding-001` | Gemini Embedding | Embedding / vector model | Semantic search, RAG | ✅ Yes | Input $0.15 |

---

## 🧑‍💻 Best Models for Code Assistants

| Model | Why Use It |
|-----|------------|
| `gemini-2.5-pro` | Strong reasoning, large context, best for coding |
| `gemini-3-pro-preview` | Frontier reasoning (preview only) |

✔ Recommended for IDE helpers, debugging, API design, architecture reasoning.

---

## 💬 Best Models for Chatbots

| Model | Scenario |
|-----|---------|
| `gemini-2.5-flash` | General-purpose chatbot |
| `gemini-2.5-flash-lite` | Massive scale, low cost |
| `gemini-3-flash-preview` | Ultra-responsive assistants |

✔ Most production chatbots should start with **2.5 Flash**.

---

## 🖼️ Best Models for Image Generation

| Model | Scenario |
|-----|---------|
| `gemini-2.5-flash-image` | Cost-effective image generation |
| `gemini-3-pro-image-preview` | Highest quality images |

✔ Image pricing depends on resolution & output tokens.

---

## 📌 Best Models for Embeddings & RAG

| Model | Use |
|-----|-----|
| `gemini-embedding-001` | Vector search, semantic similarity, RAG |

✔ Works well with **FAISS, Pinecone, Weaviate, Milvus**.

---

## 🔐 Production Recommendation

| Environment | Recommendation |
|-----------|----------------|
| Prototyping | Free tier |
| Internal tools | Flash / Flash-Lite |
| Production | Paid tier + quotas |
| Healthcare / enterprise | Paid tier + GCP controls |

---

## 📎 References
- https://ai.google.dev/gemini-api/docs/models
- https://ai.google.dev/gemini-api/docs/pricing
- https://ai.google.dev/gemini-api/docs/rate-limits

---

⭐ **Tip:**  
If you are building **chatbots, healthcare triage, or RAG pipelines**, start with  
`gemini-2.5-flash` → upgrade to `gemini-2.5-pro` only when needed.
