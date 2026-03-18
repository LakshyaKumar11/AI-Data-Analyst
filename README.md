Build Your Personal AI Data Analyts
Many Chat with your Data tools make a critical mistake: they try to make the AI answer the question directly. LLMs are bad at math. If you ask an LLM to calculate the average of 10,000 rows, it will hallucinate.

The solution is not to ask the AI to do the math. Ask the AI to write the code that does the math.

Here is the architecture we are building:

Ingest: Load any flat file (CSV, Excel, JSON).
Detect: Algorithmically understand the column types (Numeric vs. Categorical).
Reason: Convert natural language (“Show me the outliers”) into Python code (df.loc[z_score > 3]).
Execute: Run that code in a sandboxed environment and return the result.
This approach combines the linguistic power of AI with the computational precision of Python.

Prerequisites
To follow along, you need a basic Python environment. You will need the following libraries:
pip install streamlit pandas matplotlib numpy scipy openpyxl

If you want to use the local LLM features for custom queries, install Ollama and pull a model like Llama 3:
ollama pull llama3.1

Building The Brain of Our Personal AI Data Analyst
Create a file named analyst.py. This file handles the heavy lifting. It’s the engine room. We are going to break down the code provided into logical chunks.
Step 1: Robust Data Loading
Step 2: Deterministic Intelligence (Prompt Suggestions)
Step 3: The Translator
Step 4: The Execution Engine
Step 5: The LLM Connector

Building The Interface for Our Personal AI Data Analyst
Now, create a file named app.py. We will use Streamlit for the frontend. It allows us to build a data dashboard in pure Python without knowing HTML or CSS
