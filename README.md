# codecortex

⚡ Hybrid System: ML Anomaly Detector + Agentic AI Analyst
🛠️ How It Works

Anomaly Detection (ML side)

Use something like Isolation Forest or One-Class SVM on stock OHLC + volume data.

Marks timestamps where stock behavior looks “unusual.”

Contextual Analysis (Agentic AI side)

An LLM agent checks external sources (news headlines, Twitter, company reports) around anomaly time.

Summarizes possible reasons:

Earnings report

Insider trading rumors

Macro event (Fed rate hike, war news)

Justification Output

Dashboard shows:

📉 Detected anomaly in TSLA stock at 2:45 PM

📰 AI found related news: “Tesla beats earnings expectations”

🤖 AI verdict: “Spike justified by earnings” OR “No news found → possible manipulation.”

⚙️ Tech Stack

Anomaly Detection (ML)

Scikit-learn: Isolation Forest / One-Class SVM.

Data: Yahoo Finance / Alpha Vantage API.

Agentic AI

LLM (GPT, Llama, Claude, etc.)

Tools:

News API (NewsAPI.org, Google News API).

Twitter/X API for social sentiment.

Financial APIs (Finnhub, Polygon.io).

Orchestration

LangChain / LlamaIndex → lets LLM act as an agent:

Take anomaly timestamp.

Query external APIs.

Summarize justification.

Frontend

Dashboard with chart (Chart.js / Plotly).

Mark anomalies in red + justification popup.

📊 Example Hackathon Demo

Show AAPL stock with an anomaly on Oct 27, 2022.

Dashboard says:

Anomaly detected (price spike).

LLM checks news → “Apple reports record iPhone sales”.

Verdict: ✅ “Spike justified by earnings report.”

Another example:

Small-cap stock → anomaly detected.

No news → LLM flags as ⚠️ “Suspicious movement — possible pump & dump.”

🚀 Stretch Goals

Use sentiment analysis on news + tweets.

Rank anomalies by “justified vs suspicious” score.

Add an auto-report generator: “Today, 3 anomalies detected. 2 justified (earnings, Fed news), 1 unexplained (possible fraud).”
