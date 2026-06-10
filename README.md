ResearchMind is an end-to-end multi-agent research pipeline built with LangChain and powered by GPT-4o-mini. You enter a research topic, and four agents pass work between them in sequence — gathering live web data, deep-reading source pages, drafting a structured report, and then critically reviewing it. The result is a downloadable Markdown research report with a scored critique.
A Streamlit UI (app.py) gives the pipeline a polished front end with real-time step status, while pipeline.py exposes the same logic as a clean Python CLI for scripting and automation.

🗂️ Project Structure
Multi-agent-research-system/
│
├── agents.py          # Agent builders (Search, Reader) + Writer/Critic LangChain chains
├── tools.py           # LangChain tools: web_search (Tavily) and scrape_url (BeautifulSoup)
├── pipeline.py        # CLI runner — orchestrates all 4 agents end-to-end
├── app.py             # Streamlit UI with real-time pipeline status and report download
├── requirements.txt   # All Python dependencies
└── .gitignore

⚙️ Tech Stack
Layer - Technology
LLMGPT - 4o-mini (via langchain-openai) 
Agent Framework - LangChain Agents + LCEL Chains 
Web Search - Tavily Search API 
Web Scraping - BeautifulSoup4 + Requests 
UI - Streamlit 
Config - python-dotenv
