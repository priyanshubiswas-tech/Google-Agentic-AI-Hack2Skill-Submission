# 🌆 Bengaluru Pulse: An Agentic AI Platform for Real-Time Urban Intelligence

## 📖 Overview

Bengaluru — a vibrant, fast-paced metropolis — generates **millions of noisy data points** every minute: traffic snarls, civic complaints, spontaneous flash mobs, cultural events, and power cuts. All of it scattered across platforms like Twitter, WhatsApp, news reports, and user posts. The result?

> **Chaos. Noise. Delay. Missed insights.**

What if there was a **smart AI agent** that could:
- Understand and summarize multiple reports.
- Analyze images/videos to categorize events.
- Predict and alert users of unfolding incidents.
- Present this data in a clean, real-time city dashboard.

Welcome to **Bengaluru Pulse** — an **Agentic AI-powered live city monitor**, combining the power of Google Gemini, Vertex AI, and Firebase to give citizens, city officials, and planners an **intelligent and unified pulse of the city**.

---

## 🎯 Problem Statement

> **Managing City Data Overload**  
Too much unstructured, real-time data — scattered across platforms, outdated quickly, and too noisy for action.

---

## 🧠 Our Solution: Agentic AI Platform

Using Google AI and Firebase, we built an **intelligent, autonomous agent** that:

- Fuses real-time, **disparate data sources** (social media, user reports).
- Uses **Gemini’s multimodal AI** to summarize, categorize, and describe city events.
- Provides **predictive insights** by learning from historical trends.
- Shows all insights on a real-time, **map-based dashboard** with alert subscriptions.

---

## 🧩 Key Features

| Feature | Description |
|--------|-------------|
| 🔄 **Data Fusion & Summarization** | Aggregates multiple similar posts using Gemini to avoid duplicates. |
| 🖼️ **Multimodal Reporting** | Users can upload geo-tagged photos/videos. Gemini processes and maps them. |
| 📡 **Predictive Alerts** | Uses event clusters to forecast outages, protests, etc. |
| 🗺️ **Live Map Dashboard** | Map with real-time event markers, sentiment heatmap, and filters. |
| 🔔 **User Notifications** | Subscribe to AI-generated summaries for your area. |

---

## 🔧 Tech Stack

### 🧠 AI / Agentic Layer
- **Google Gemini Pro** (via Vertex AI): Summarization, NLU, image/video understanding
- **Vertex AI**: Custom model deployment for predictions
- **AI Studio**: Prompt development & testing

### ☁️ Backend / Cloud
- **Firebase Firestore**: Real-time DB for events, users
- **Firebase Storage**: Upload geo-tagged photos/videos
- **Cloud Functions**: Trigger AI summarization, data processing
- **Pub/Sub**: Scalable data ingestion from APIs/social feeds
- **BigQuery**: Historical trend analysis, training data

### 🌍 Frontend / Visualization
- **React.js + TailwindCSS**: Clean UI for map & dashboard
- **Mapbox SDK**: Real-time map & overlays
- **Firebase Hosting**: Deployed frontend
- **Firebase Auth**: User login, area subscriptions

---

## 🔁 System Architecture (Mermaid)

```mermaid
graph TD
  A[User Submission / External Feeds] --> B[Firebase Functions]
  B --> C[Pub/Sub Queue]
  C --> D[Vertex AI - Gemini]
  D --> E1[Summarized Event in Firestore]
  D --> E2[Image/Video Analysis → Event Classification]
  E1 --> F[Live Map Dashboard (React)]
  E2 --> F
  F --> G[Push Notifications to Users]
  G --> H[User Subscriptions (Firestore)]
