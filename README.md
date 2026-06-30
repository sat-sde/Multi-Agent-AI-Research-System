# 🔬 ResearchMind — Multi-Agent AI Research System

> A powerful multi-agent AI pipeline that autonomously searches, scrapes, writes, and critiques research reports on any topic — powered by **Google Gemini 2.5 Flash** and **Tavily Search**.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.37+-red?style=flat-square&logo=streamlit)
![LangChain](https://img.shields.io/badge/LangChain-0.2+-green?style=flat-square)
![LangGraph](https://img.shields.io/badge/LangGraph-0.1+-purple?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 🧠 How It Works

Four specialized AI agents collaborate in a sequential pipeline:

```
User Topic
    │
    ▼
┌─────────────────┐
│  01 Search Agent │  ── Finds recent web info via Tavily Search
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  02 Reader Agent │  ── Scrapes top URLs for deep content
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  03 Writer Chain │  ── Drafts a full structured research report
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  04 Critic Chain │  ── Reviews, scores & gives feedback
└─────────────────┘
         │
         ▼
  📄 Final Report (downloadable .md)
```

---

## ✨ Features

- 🔍 **Real-time Web Search** — via Tavily API (live results)
- 📄 **Deep Content Scraping** — extracts clean text from top URLs
- ✍️ **AI Report Writing** — structured with Introduction, Key Findings & Conclusion
- 🧐 **Critic & Scoring** — rates the report out of 10 with actionable feedback
- ⬇️ **Download Report** — export the final report as a `.md` file
- 🎨 **Beautiful UI** — dark mode Streamlit app with premium design
- ☁️ **Streamlit Cloud Ready** — one-click deployment

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **LLM** | Google Gemini 2.5 Flash (free tier) |
| **Agent Framework** | LangGraph + LangChain |
| **Web Search** | Tavily Search API (free tier) |
| **Web Scraping** | BeautifulSoup4 + Requests |
| **UI** | Streamlit |
| **Language** | Python 3.10+ |

---

## 🚀 Quick Start (Local)

### 1. Clone the repo

```bash
git clone https://github.com/sat-sde/Multi-Agent-AI-Research-System.git
cd Multi-Agent-AI-Research-System
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up API Keys

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_google_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
```

> 🆓 **Both APIs have free tiers:**
> - Google Gemini → [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
> - Tavily → [app.tavily.com](https://app.tavily.com) (1000 searches/month free)

### 4. Run the app

```bash
streamlit run app.py
```

Open **http://localhost:8501** in your browser.

---

## ☁️ Deploy on Streamlit Cloud

1. Fork this repo on GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in
3. Click **New app** → select this repo → set `app.py` as main file
4. In **Advanced Settings → Secrets**, add:

```toml
GOOGLE_API_KEY = "your_google_api_key_here"
TAVILY_API_KEY = "your_tavily_api_key_here"
```

5. Click **Deploy!** 🎉

---

## 📁 Project Structure

```
Multi-Agent-AI-Research-System/
│
├── app.py            # Main Streamlit UI
├── agents.py         # LangGraph agent & chain definitions
├── tools.py          # Web search & URL scraper tools
├── pipeline.py       # Pipeline orchestration logic
├── requirements.txt  # Python dependencies
├── .env              # API keys (local only, not committed)
└── .gitignore        # Excludes .env and __pycache__
```

---

## 🔑 Environment Variables

| Variable | Description | Where to Get |
|----------|-------------|-------------|
| `GOOGLE_API_KEY` | Google Gemini API key | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) |
| `TAVILY_API_KEY` | Tavily Search API key | [app.tavily.com](https://app.tavily.com) |

---

## 📸 Demo

Enter any topic → watch the 4-agent pipeline run → get a polished research report:

- **"LLM agents 2025"**
- **"CRISPR gene editing breakthroughs"**
- **"Fusion energy progress"**

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

---

## 📄 License

MIT License — feel free to use and modify.

---

<div align="center">
  Built with ❤️ using LangChain · LangGraph · Streamlit · Google Gemini
</div>
