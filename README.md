# 🍽️ MaRGen-Inspired Multi-Agent Restaurant Market Analysis

A **MaRGen-inspired multi-agent system** that performs **automated market research and sales optimization** for restaurant businesses using collaborative LLM agents.

This system demonstrates how **multiple specialized AI agents** work together like a consulting team — retrieving data, analyzing trends, writing insights, and refining recommendations — with **minimal human input**.

---

## 👥 Team Members (Team 4)

| Name | Role |
|------|------|
| **Vaibhavi Shinde** | Data Set Curation, Research & Presentation |
| **Deepak Reddy** | Model + Demo Integration |
| **Ganesh Paparaju** | Agent Pipeline + UI Development |

---

## 🎯 Project Goal

Traditional market research is **slow, expensive, and requires human analysts**.

Inspired by the **MaRGen (2025)** research paper from Amazon Science, this project aims to:

✅ Automate end-to-end data analysis workflows  
✅ Generate professional market insight reports  
✅ Provide actionable strategy recommendations for sales optimization  
✅ Reduce time and cost of market research from days to minutes  

---

## 🧠 System Architecture
```
User Query (Business Problem)
         ↓
[Retriever Agent] → Retrieves relevant records from Yelp & Menu Sales datasets
         ↓
[Researcher Agent] → Analyzes data to extract insights (revenue, top items, trends)
         ↓
[Writer Agent] → Creates consulting-style business report with recommendations
         ↓
[Reviewer Agent] → Polishes clarity, flow, and adds strategic recommendations
         ↓
[Streamlit UI] → Displays insights, reports step-by-step
```

---

## 📂 Tech Stack

| Component | Tool |
|-----------|------|
| **UI** | Streamlit |
| **LLM Agents** | Local LLMs via Ollama (llama3.1 / mistral / qwen) |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Python 3.11+ |

---

## 📊 Dataset

The demo uses restaurant business and menu sales data:
```
data/
├── Hybrid_Yelp_Restaurant_Sales.csv  # Restaurant ratings, reviews, locations
└── Menu_Sales_Data.csv               # Menu items, revenue, categories, dates
```

**Dataset Statistics:**
- **3,600 Yelp reviews** across 15 restaurants
- **3,120 menu transactions** with sales data
- Multiple cuisine categories and price points

---

## 🚀 Running the Demo

### 1️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 2️⃣ Install Ollama & Pull Model
```bash
# Install Ollama from https://ollama.ai
ollama pull llama3.1
```

### 3️⃣ Launch the Application
```bash
streamlit run app.py
```

The app will open in your browser at `http://localhost:8501`

---

## 💡 Key Features

🔹 **Automated Data Retrieval** – Intelligent agent queries datasets based on user questions  
🔹 **Multi-Dimensional Analysis** – Revenue trends, top performers, category insights  
🔹 **Professional Reports** – Consulting-style markdown reports with executive summaries  
🔹 **Iterative Refinement** – Reviewer agent improves clarity and actionability  
🔹 **Visual Insights** – Automated chart generation for key metrics  

---

## 📈 Example Use Cases

1. **"Which menu categories are underperforming in sales and provide recommendations to improve performance?"**
2. **"Analyze revenue trends across different cuisines and suggest optimization strategies."**
3. **"Identify top-performing restaurants and extract success factors."**

---

## 🔬 Inspired by MaRGen Research

This implementation is based on the **MaRGen (Market Report Generator)** research paper that demonstrates:
- Multi-agent collaboration for market research
- Iterative quality improvement (reaching 10/10 scores in 3-4 rounds)
- LLM-as-judge evaluation correlating with human experts (r=0.6, p<0.01)
- Cost-effective analysis (~$1 per 6-page report, ~7 minutes)

---

## 📝 Project Structure
```
MaRGen-MultiAgent-Restaurant-Analysis/
├── app.py                    # Streamlit UI
├── agents/
│   ├── retriever.py         # Data retrieval agent
│   ├── researcher.py        # Analysis agent
│   ├── writer.py            # Report generation agent
│   └── reviewer.py          # Quality improvement agent
├── data/                    # Datasets
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

---

## 🎓 Course Context

**Course:** DAMG 7374-02 - Data Engineering: Impact of Generative AI with LLM’s 
**Institution:** Northeastern University  
**Semester:** Fall 2025

---

## 🚀 Future Enhancements

- Integration with real-time data pipelines (Snowflake/APIs)
- Deploy as interactive consulting assistant
- Add more specialized agents for deeper domain reasoning
- Expand to other industries (retail, e-commerce)

---

## 📄 License

This project is for educational purposes as part of coursework at Northeastern University.

---

## 🙏 Acknowledgments

Special thanks to the Amazon Science team for the MaRGen research paper that inspired this implementation.
