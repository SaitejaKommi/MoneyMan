# 🏦 MoneyMan — AI-Powered Digital Wealth Advisory Avatar

> **Built for IDBI Innovate 2026 — Track 01: AI-Powered Digital Wealth Advisory**
> 
> **Live Production Link:** [https://moneyman-27st.onrender.com/](https://moneyman-27st.onrender.com/)

---

## 💡 The Core Vision

Wealth advisory in standard banking applications remains fragmented, static, and disconnected from real-time customer behaviors. Customers are forced to fill out long, tedious risk-assessment forms, which leads to high drop-offs and outdated advice.

**MoneyMan** redefines this paradigm by serving as a seamless plug-and-play module for the IDBI ecosystem. Rather than asking questions, it silently builds a dynamic **"Financial Behaviour Twin"** of the customer by parsing their transaction history. It scores their risk category, analyzes spending trends, and offers proactive, explainable advice.

---

## 🌟 The "Wow" Factors (Hackathon Highlights)

### 1. Dynamic Financial Behaviour Twin
Instead of static risk forms, MoneyMan continuously analyzes 6 months of historical transactions. It automatically calculates:
*   **Risk Profile & Category** (Conservative, Moderate, Aggressive).
*   **Asset Ratios** (Investment-to-Income, Savings-to-Income, Spending-to-Income).
*   **Spend Anomalies** (e.g., alert when dining spend spikes by 132% or SIP reduces by 53%).

### 2. Live Conversational Advisor with Audio Feedback
A friendly, interactive wealth assistant powered by:
*   **Groq (Llama-3.1-8B)**: Near-zero latency response generation.
*   **WebSpeech API**: Native, local browser text-to-speech engine ensuring zero server latency and **zero marginal cost** per audio stream.
*   **Interactive State Animations**: The avatar dynamically transitions between *Idle*, *Listening*, and *Speaking* states, synced directly with WebSpeech API events.

### 3. Fully Explainable Advisory Engine
To comply with financial regulations and audit guidelines, every single suggestion provided by the AI has a clear **Triggers** list. If MoneyMan suggests increasing a SIP or shifting capital to debt funds, it clearly exposes the "Why" (e.g., *Trigger: Savings rate has declined by 60%*).

### 4. Interactive "What-If" Goal Simulator
A visual tool showing the long-term impact of monthly saving decisions. Users adjust a fluid range slider to simulate changes in their monthly investment (SIP). The charts and months-to-goal progress update in real-time with automatic warnings if they fall behind schedule.

### 5. Premium Neo-Bento Design System
Designed to meet global Visa/Mastercard aesthetic standards:
*   Modern Soft-Brutalist "Bento Grid" layout.
*   Massive typography (`font-weight: 900`) for clear financial legibility.
*   Massive, tactile rounded card layouts (`32px`–`40px`).
*   Global unified **Light & Dark mode** toggle accessible from the sidebar.

---

## 🛠️ Technology Stack

*   **Frontend**: React 18, Vite 5, Recharts (for charts), Framer Motion (for fluid animations), Web Speech API.
*   **Backend**: Express 5, Node.js (REST APIs, profiling, and recommendation generation engines).
*   **AI Engine**: Groq Cloud SDK.
*   **Styles**: Modern Vanilla CSS variables with custom theme tokens.

---

## ⚙️ Local Setup Instructions

Follow these steps to run the application locally on your machine.

### Prerequisites
*   [Node.js](https://nodejs.org/) (v18 or higher recommended)
*   npm (installed automatically with Node)

### 1. Clone the Repository
```bash
git clone https://github.com/Durgaprasad-Developer/MoneyMan.git
cd MoneyMan
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Up Environment Variables
Create a file named `.env` in the root directory:
```bash
GROQ_API_KEY=your_groq_api_key_here
```
*(Get your free API key from [Groq Console](https://console.groq.com/))*

### 4. Start the Application
Run the concurrent development command which launches both the Express backend server (port `3001`) and the Vite React frontend server (port `5173`):
```bash
npm run dev
```

Open your browser and navigate to the local address displayed in the console (usually `http://localhost:5173`).

---

## 🚀 Production Deployment Configuration

This repository is optimized for deployment as a single **monolithic web service** on platforms like Render, Railway, or Heroku. The Express backend is configured to automatically build and serve the static React frontend folder (`dist/`) in a production environment.

### Deployment settings:
*   **Build Command**: `npm install && npm run build`
*   **Start Command**: `node server/index.js`
*   **Environment Variables**:
    *   `GROQ_API_KEY`: *(your live Groq SDK key)*
    *   `NODE_ENV`: `production`

---

## 📂 Project Structure

```
├── dist/                   # Compiled static production build assets
├── server/                 # Express backend APIs & engines
│   ├── data/               # Mock data payloads
│   ├── engines/            # Profiling and recommendation logic
│   └── index.js            # Express server entry point
├── src/                    # React frontend application
│   ├── components/         # Neo-Bento UI modules (Dashboard, Chat, Goals, Profile, Nudges)
│   ├── context/            # Global state and Theme context
│   ├── hooks/              # Custom React hooks (API handlers, Speech hooks)
│   ├── utils/              # Colors, constants, and endpoints
│   ├── App.jsx             # Shell layout and navigation
│   └── index.css           # Design system root tokens (radii, grid alignments, light/dark themes)
└── Product_Report.pdf      # Detailed hackathon submission artifact
```

---

*Built with ❤️ by Team MoneyMan for the IDBI Innovate Hackathon 2026.*
