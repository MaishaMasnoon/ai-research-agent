AI Research Agent with LangChain

**Overview**

This project implements an intelligent AI research agent using LangChain and OpenAI models. The agent autonomously gathers information from multiple tools, synthesizes insights, and returns structured research outputs.

**Features**
- Tool-augmented LLM agent (web search, Wikipedia, file output)
- Structured responses using Pydantic schema validation
- Dynamic prompt engineering with enforced output formatting
- Modular tool integration for extensibility
- JSON-based research summaries for downstream processing

**Architecture**

The system uses a tool-calling agent architecture:

LLM: OpenAI Chat model

Agent Framework: LangChain Agent Executor

Tools:
- Web search
- Wikipedia lookup
- File writer

Output Parser: Pydantic-based schema enforcement

**Example Output**

{

  "topic": "Artificial Intelligence in Healthcare",
  "summary": "...",
  "sources": ["Wikipedia", "Web Search"],
  "tools_used": ["wiki_tool", "search_web"]

}

**Setup**
1. Clone the repo
git clone https://github.com/YOUR_USERNAME/ai-research-agent.git
cd ai-research-agent
2. Install dependencies
pip install -r requirements.txt
3. Configure environment

Create a .env file:

OPENAI_API_KEY=your_api_key

OPENAI_MODEL=gpt-4o-mini

**Run the Agent**

python main.py

**Example Usage**

Enter a research topic: Impact of climate change on agriculture

**Future Improvements**

- Add conversational memory
- Deploy as FastAPI service
- Integrate LangSmith tracing
- Add evaluation metrics for response quality

**Tech Stack**

- Python
- LangChain
- OpenAI API
- Pydantic
- dotenv

**Author**

Maisha Masnoon