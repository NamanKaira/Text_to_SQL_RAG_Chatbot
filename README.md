🧠 Text-to-SQL GenAI System (Gemini + LangChain + RAGAS)

Convert natural language questions into SQL queries using Google Gemini API, LangChain, and evaluate performance using RAGAS metrics.

🚀 Project Overview

This project implements a GenAI-powered Text-to-SQL pipeline that allows users to:

Ask questions in natural language
Automatically generate SQL queries
Query a MySQL database
Evaluate the quality of generated queries using RAGAS
🏗️ Architecture
User Question
     ↓
Prompt Template (LangChain)
     ↓
Gemini LLM (SQL Generation)
     ↓
Generated SQL Query
     ↓
(Optional: Execute on MySQL DB)
     ↓
Evaluation using RAGAS
⚙️ Tech Stack
LLM: Google Gemini API
Framework: LangChain
Database: MySQL
Evaluation: RAGAS
Embeddings: HuggingFace (sentence-transformers)
Language: Python
📂 Project Structure
📦 Text-to-SQL-GenAI
 ┣ 📜 notebook.ipynb
 ┣ 📂 data
 ┣ 📜 requirements.txt
 ┗ 📜 README.md
🔧 Setup Instructions
1. Clone the Repository
git clone https://github.com/your-username/text-to-sql-genai.git
cd text-to-sql-genai
2. Create Environment
conda create -n genai_sql python=3.10
conda activate genai_sql
3. Install Dependencies
pip install -r requirements.txt

If needed:

pip install sentence-transformers langchain-google-genai pymysql ragas
4. Setup API Key

Get your API key from Google AI Studio and set it:

import os
os.environ["GOOGLE_API_KEY"] = "your_api_key_here"
5. Setup MySQL Database

Update connection details:

host = 'localhost'
port = '3306'
username = 'root'
password = 'your_password'
database_schema = 'your_database'
6. Run the Notebook

Open Jupyter Notebook:

jupyter notebook

Run all cells step by step.

💡 Example

Input:

What was the budget of Product 12?

Generated SQL:

SELECT `2017 Budgets` FROM `2017_budgets` WHERE `Product Name` = 'Product 12'
📊 Evaluation (RAGAS)
Metric	Score
Context Precision	0.80
Helpfulness	4.6 / 5
🎯 Features
Natural language → SQL conversion
Schema-aware query generation
Works with MySQL databases
Evaluation using RAGAS metrics
Modular LangChain pipeline
⚠️ Limitations
No UI (currently notebook-based)
Limited dataset size
No SQL execution validation layer
Requires manual setup
🔮 Future Improvements
Add Streamlit UI for interaction
Execute generated SQL and display results
Add error handling & query correction
Deploy as a web app
Expand dataset for better evaluation
