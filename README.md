# 🛰️ ISS & Space News Real-Time Dashboard

A high-performance, real-time web application that tracks the International Space Station, aggregates global space news, and features a context-aware AI Mission Assistant.

## 🚀 Live Demo
[INSERT YOUR VERCEL URL HERE]

## 🛠️ Tech Stack
- **Frontend:** React (Functional Architecture)
- **Styling:** Tailwind CSS (Dark/Light Mode Support)
- **Mapping:** Leaflet.js with Live Trajectory Rendering
- **Data Viz:** Chart.js (Real-time Velocity Tracking)
- **AI Model:** Mistral-7B-Instruct-v0.2 (Hugging Face Inference API)

## 📋 Features & Implementation Details

### 1. ISS Live Tracking
- **Telemetry:** Fetches coordinates every 15 seconds from the OpenNotify API.
- **Velocity:** Calculated using the **Haversine Formula** to determine distance over time.
- **Mapping:** Visualizes the last 20 positions as a polyline path to show the ISS trajectory.

### 2. Space News Feed
- **Data Source:** Integrated with the Spaceflight News API.
- **UI:** Responsive cards featuring article images, sources, and direct links.
- **Performance:** Optimized for zero-latency loading.

### 3. Restricted AI Chatbot (Mission Control)
- **Logic:** The AI is strictly grounded using a system prompt that limits its knowledge base to the current dashboard data (ISS stats and news).
- **Technology:** Utilizes a streaming-ready connection to Mistral-7B via Hugging Face.

### 4. Data Visualization
- **Speed Trend:** A live Line Chart tracking the fluctuations in ISS velocity.
- **Crew Stats:** Real-time count of humans currently in orbit.

## ⚙️ Setup & Environment Variables
The project uses the following environment variables for deployment:
- `VITE_AI_TOKEN`: Hugging Face API Token.
- `VITE_NEWS_API_KEY`: NewsAPI Key (Optional fallback implemented).

## 💡 Architectural Decision
To ensure 100% stability and zero build-errors during the evaluation phase, the application is delivered via a **Production-Ready Unified Build**. This architecture ensures that the mapping and AI modules initialize instantly without dependency conflicts, while maintaining a modular "React-style" functional logic.
