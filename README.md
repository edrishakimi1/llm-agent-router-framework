# LLM Agent Framework: Intelligent Customer Routing

An Python-based routing system that uses Large Language Models to classify customer queries and route them to the appropriate service agents.

##  Project Overview
This framework solves the problem of manual query sorting by implementing an LLM-based Router. It intelligently directs users to either an FAQ Agent or an Order Status Agent based on intent.



## Quick Start

### 1. Prerequisites
* Python 3.9+
* API Keys for Groq and Google Gemini.

### 2. Installation
```bash
git clone https://github.com/edrishakimi1/llm-agent-router-framework.git
cd llm-agent-framework
pip install pandas openai python-dotenv


---

### 3. Environment Configuration

Create a `.env` file in the project root to securely store your API keys:

```env
GROQ_API_KEY=your_groq_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here
```

---

### 4. Running the Project

All routing logic, evaluation code, and results are contained in the Jupyter Notebook. To launch it:

```bash
jupyter notebook routing_patterns.ipynb
```

---

##  Evaluation Criteria & Results

The routing models were evaluated using a ground-truth dataset across the following dimensions:

* **Accuracy** – Correctly selecting the appropriate agent
* **Average Latency** – Inference time in seconds
### Model Comparison

| Metric       | Llama-3.3-70B (Groq) | Gemini-2.5-Flash-Lite |
| ------------ | -------------------- | --------------------- |
| Accuracy     | 100%                 | 100%                  |
| Avg. Latency | **0.255s ⚡**         | 0.511s                |

---

##  Conclusion

**Recommended Model:** Llama-3.3-70B (via Groq)

### Why?

Although both models achieved perfect accuracy, **Llama-3.3-70B on Groq** clearly outperforms in a production setting:

*  **2× faster inference latency**, ensuring a responsive user experience

For these reasons, Llama-3.3-70B is the preferred choice for deploying this LLM-based customer routing framework in production environments.




