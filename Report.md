Changed below fields,
TOP_K from 4 to 5.
CHUNK_OVERLAP = 350
EMBEDDING_MODEL = "all-MiniLM-L12-v2"

It had helped with as answer were more modified and more concise.


Output :

You: can you analyze Montly economic report of india and highlight which fields had better growth

Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 8591.70it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
/Users/rasikarasal/RAG_AI_Agent_Assignment/RAG_AI_Agent_Assignment/rag_agent.py:117: LangChainDeprecationWarning: The class `Chroma` was deprecated in LangChain 0.2.9 and will be removed in 1.0. An updated version of the class exists in the `langchain-chroma package and should be used instead. To use it run `pip install -U `langchain-chroma` and import as `from `langchain_chroma import Chroma``.
  vector_store = Chroma(
    Score: 0.378 | data/Monthly Economic Review August 2025.pdf
    Score: 0.378 | data/Monthly Economic Review August 2025.pdf
    Score: 0.375 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.375 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.360 | data/Monthly Economic Review August 2025.pdf
  [Retrieve] Found 5 relevant chunks for: 'can you analyze Montly economic report of india and highlight which fields had better growth'
    [1] data/Monthly Economic Review August 2025.pdf (Page 5)
    [2] data/Monthly Economic Review August 2025.pdf (Page 5)
    [3] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [4] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [5] data/Monthly Economic Review August 2025.pdf (Page 26)
  [Generate] Answer produced.

Assistant: Based on the Monthly Economic Review August 2025, here is the analysis of India's economic growth in Q1 FY26:

### Key Growth Highlights:
- **Real GDP growth:** India’s real GDP grew by **7.8% YoY**, marking a five-quarter high.
- **Real Gross Value Added (GVA):** Expanded by **7.6% YoY**.
- **Nominal GDP and GVA:** Both grew by **8.8% YoY**.
- India’s growth rate is the fastest among peers, notably higher than China (**5.2%**) and Indonesia (**5.1%**).

### Sectoral Growth:
- The report mentions a **healthy performance across sectors**.
- Real GVA growth in the **industry sector** picked up, driven by:
  - Strong product demand.
  - Deeper engagement with merchant partners.
- GDP growth was primarily anchored by **domestic drivers**.

### Summary Table:

| Indicator                  | Growth Rate (YoY) | Notes                          |
|----------------------------|-------------------|--------------------------------|
| Real GDP                   | **7.8%**          | Five-quarter high              |
| Real GVA                   | **7.6%**          | Broad sectoral growth          |
| Nominal GDP & GVA          | **8.8%**          | Reflects price and volume growth|
| Industry Sector GVA Growth | Picked up         | Driven by product demand & merchant engagement |

### Potential Risks/Assumptions:
- Global economic and policy uncertainty remains elevated.
- Growth is heavily reliant on domestic demand.
- External factors like global trade tensions or commodity price shocks could impact momentum.

### Improvements/Opportunities:
- Continued reform push could further enhance growth prospects.
- Upgrades in sovereign credit rating (from BBB to BBB+) indicate improved economic stability and investor confidence.

---

**Sources:**
- Monthly Economic Review August 2025, Page 5

------------------------------------------------------------

You: quit
Goodbye!
➜  RAG_AI_Agent_Assignment git:(main) ✗ python3 ingestion.py
==================================================
STEP 1: DATA EXTRACTION (PDF Loading)
==================================================
  Loading: RIL-Integrated-Annual-Report-2024-25.pdf
  Loading: Monthly Economic Review August 2025.pdf
  Loading: infosys-ar-25.pdf
  Loaded 546 pages from 3 PDF(s).

==================================================
STEP 2: CHUNKING (Text Splitting)
==================================================
  Split into 3442 chunks (size=1000, overlap=350).

==================================================
STEP 3: CREATE VECTOR DB (ChromaDB)
==================================================
Warning: You are sending unauthenticated requests to the HF Hub. Please set a HF_TOKEN to enable higher rate limits and faster downloads.
Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 8397.98it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
  Vector store created at 'chroma_db/' with 3442 vectors.

Ingestion complete!
➜  RAG_AI_Agent_Assignment git:(main) ✗ python3 main.py
============================================================
       RAG AI Agent - LangGraph + ChromaDB
============================================================

Using vector database at 'chroma_db/'.

============================================================
       RAG Agent Ready - Ask Questions!
============================================================
Type your question and press Enter. Type 'quit' to exit.

You: can analyze monthly econmoic report for august 2025 and give few insights on it

Warning: You are sending unauthenticated requests to the HF Hub. Please set a HF_TOKEN to enable higher rate limits and faster downloads.
Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 8318.05it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
/Users/rasikarasal/RAG_AI_Agent_Assignment/RAG_AI_Agent_Assignment/rag_agent.py:117: LangChainDeprecationWarning: The class `Chroma` was deprecated in LangChain 0.2.9 and will be removed in 1.0. An updated version of the class exists in the `langchain-chroma package and should be used instead. To use it run `pip install -U `langchain-chroma` and import as `from `langchain_chroma import Chroma``.
  vector_store = Chroma(
    Score: 0.510 | data/Monthly Economic Review August 2025.pdf
    Score: 0.510 | data/Monthly Economic Review August 2025.pdf
    Score: 0.510 | data/Monthly Economic Review August 2025.pdf
    Score: 0.415 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.415 | data/RIL-Integrated-Annual-Report-2024-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'can analyze monthly econmoic report for august 2025 and give few insights on it'
    [1] data/Monthly Economic Review August 2025.pdf (Page 1)
    [2] data/Monthly Economic Review August 2025.pdf (Page 1)
    [3] data/Monthly Economic Review August 2025.pdf (Page 1)
    [4] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 22)
    [5] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 22)
  [Generate] Answer produced.

Assistant: The provided context includes the cover page of the "Monthly Economic Review August 2025" from the Economic Division but does not contain any detailed economic data, analysis, or insights from the report itself.

Therefore, I am unable to analyze the Monthly Economic Review for August 2025 or provide insights based on the current information.

If you can provide specific pages or sections with economic data or commentary from the report, I would be happy to analyze and summarize the insights for you.

Sources:
- Monthly Economic Review August 2025.pdf (Page 1)

------------------------------------------------------------

You: quit
Goodbye!
➜  RAG_AI_Agent_Assignment git:(main) ✗ python3 ingestion.py
==================================================
STEP 1: DATA EXTRACTION (PDF Loading)
==================================================
  Loading: RIL-Integrated-Annual-Report-2024-25.pdf
  Loading: Monthly Economic Review August 2025.pdf
  Loading: infosys-ar-25.pdf
  Loaded 546 pages from 3 PDF(s).

==================================================
STEP 2: CHUNKING (Text Splitting)
==================================================
  Split into 3442 chunks (size=1000, overlap=350).

==================================================
STEP 3: CREATE VECTOR DB (ChromaDB)
==================================================
Warning: You are sending unauthenticated requests to the HF Hub. Please set a HF_TOKEN to enable higher rate limits and faster downloads.
Loading weights: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 13244.68it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
  Vector store created at 'chroma_db/' with 3442 vectors.

Ingestion complete!
➜  RAG_AI_Agent_Assignment git:(main) ✗ python3 main.py     
============================================================
       RAG AI Agent - LangGraph + ChromaDB
============================================================

Using vector database at 'chroma_db/'.

============================================================
       RAG Agent Ready - Ask Questions!
============================================================
Type your question and press Enter. Type 'quit' to exit.

You: can you analyze Montly economic report of india and highlight which fields had better growth in 2025

Warning: You are sending unauthenticated requests to the HF Hub. Please set a HF_TOKEN to enable higher rate limits and faster downloads.
Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 8853.53it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
/Users/rasikarasal/RAG_AI_Agent_Assignment/RAG_AI_Agent_Assignment/rag_agent.py:117: LangChainDeprecationWarning: The class `Chroma` was deprecated in LangChain 0.2.9 and will be removed in 1.0. An updated version of the class exists in the `langchain-chroma package and should be used instead. To use it run `pip install -U `langchain-chroma` and import as `from `langchain_chroma import Chroma``.
  vector_store = Chroma(
    Score: 0.472 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.472 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.472 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.472 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.455 | data/RIL-Integrated-Annual-Report-2024-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'can you analyze Montly economic report of india and highlight which fields had better growth in 2025'
    [1] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [2] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [3] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [4] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 7)
    [5] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
  [Generate] Answer produced.

Assistant: The provided context does not contain information about the Monthly Economic Report of India or detailed sector-wise growth data for 2025. However, from the financial performance data of Reliance Industries Limited for FY 2024-25, we can infer some growth trends related to their business segments:

### Key Growth Highlights for FY 2024-25 (Reliance Industries Limited):
- **Value of sales and services** increased by **7.9%** to **₹3,30,943 crore** from ₹3,06,848 crore in FY 2023-24.
- **Revenue from operations** grew by **6.6%** to **₹2,91,043 crore** from ₹2,73,131 crore.
- **EBITDA** rose by **8.6%** to **₹25,094 crore** from ₹23,108 crore.
- **EBITDA margin** improved slightly by **10 basis points** to **8.6%** from 8.5%.

### Sectoral Insights:
- Growth trajectory was driven by **strong product demand** and **deeper engagement with merchant partners**.
- However, the **operating margin ratio declined to 7.2%** from 9.8% primarily due to **weaker transportation fuels and downstream chemical margins**.
- Return on net worth fell to 8.2% from 10.3%, indicating some pressure on overall profitability.

### Macro Environment:
- The first half of FY 2024-25 saw **healthy growth momentum** in India, supported by fiscal health improvements and stable currency.
- The second half experienced **large outflows from foreign portfolio investors** and softening growth, indicating some volatility.

### Summary:
- The **strongest growth** was seen in **product demand and merchant engagement** areas.
- **Transportation fuels and downstream chemicals** faced margin pressures.
- Overall, the company showed **moderate revenue and EBITDA growth** with slight margin improvement.

### Limitations:
- No comprehensive monthly economic report or sector-wise growth data for India in 2025 is provided.
- The analysis is limited to Reliance Industries Limited's financial performance and macroeconomic commentary.

---

**Sources:**
- Reliance Industries Limited Integrated Annual Report 2024-25, Pages 6-7 (Documents [1] to [5])

------------------------------------------------------------

You: can see potential market risk for RIL report   

Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 7484.86it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
    Score: 0.528 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.528 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.528 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.528 | data/RIL-Integrated-Annual-Report-2024-25.pdf
    Score: 0.511 | data/RIL-Integrated-Annual-Report-2024-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'can see potential market risk for RIL report'
    [1] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
    [2] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
    [3] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
    [4] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
    [5] data/RIL-Integrated-Annual-Report-2024-25.pdf (Page 2)
  [Generate] Answer produced.

Assistant: The provided context from the Reliance Industries Limited (RIL) Integrated Annual Report 2024-25 does not explicitly detail specific potential market risks faced by RIL. However, based on the information available, some inferred potential market risks could include:

- **Capital Allocation Risks**: RIL emphasizes prudent capital allocation within a robust risk management framework, indicating that improper capital deployment could pose risks to achieving strategic goals.
- **Retail Market Risks**: With a large retail footprint of **19,340 retail stores** and **77.4 million sq. ft.** retail area, risks could arise from changes in consumer behavior, competition, or economic downturns affecting retail sales.
- **Customer Base and Transaction Volume**: Managing a registered customer base of over **349 million** and approximately **1.4 billion transactions** involves operational risks, including data security, customer retention, and transaction processing.
- **People Management**: With **247,782 people** employed, risks related to human capital such as labor disputes, talent retention, and productivity could impact operations.

Since the report mentions a "robust risk management framework," it implies that RIL is aware of and actively managing these and other risks, but specific market risks are not detailed in the provided excerpts.

### Summary Table of Potential Market Risks (Inferred)

| Risk Area               | Description                                                  |
|------------------------|--------------------------------------------------------------|
| Capital Allocation      | Risk of suboptimal investment impacting strategic goals      |
| Retail Market          | Consumer behavior shifts, competition, economic downturns    |
| Customer & Transactions | Data security, customer retention, transaction processing    |
| Human Capital          | Labor disputes, talent retention, productivity issues        |

### Potential Downsides or Assumptions
- The analysis is based on limited information; detailed risk disclosures are likely in other sections of the full report.
- Market risks could also include macroeconomic factors, regulatory changes, and technological disruptions not covered here.

If you need a detailed risk analysis, I recommend reviewing the "Risk and Governance" section of the full RIL Annual Report.

Sources:
- [1] RIL-Integrated-Annual-Report-2024-25.pdf (Page 6)
- [5] RIL-Integrated-Annual-Report-2024-25.pdf (Page 2)

------------------------------------------------------------

You: keyhighlights for Performance overview for infosys report

Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 6613.00it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
    Score: 0.422 | data/infosys-ar-25.pdf
    Score: 0.422 | data/infosys-ar-25.pdf
    Score: 0.422 | data/infosys-ar-25.pdf
    Score: 0.422 | data/infosys-ar-25.pdf
    Score: 0.394 | data/infosys-ar-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'keyhighlights for Performance overview for infosys report'
    [1] data/infosys-ar-25.pdf (Page 244)
    [2] data/infosys-ar-25.pdf (Page 244)
    [3] data/infosys-ar-25.pdf (Page 244)
    [4] data/infosys-ar-25.pdf (Page 244)
    [5] data/infosys-ar-25.pdf (Page 9)
  [Generate] Answer produced.

Assistant: The provided context does not contain specific details or key highlights related to the "Performance overview" section of the Infosys Integrated Annual Report 2024-25. The excerpts mainly focus on expense details such as cost of software packages, third-party items, other expenses, and employee benefits accounting policy.

For a comprehensive summary of the performance overview, additional sections of the report would be needed that specifically discuss financial results, revenue growth, profitability, operational achievements, and strategic initiatives.

Sources:
- Infosys Integrated Annual Report 2024-25, Page 244
- Infosys Integrated Annual Report 2024-25, Page 9

------------------------------------------------------------

You: Performance Overview of Infosys report

Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 7098.23it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
    Score: 0.666 | data/infosys-ar-25.pdf
    Score: 0.666 | data/infosys-ar-25.pdf
    Score: 0.666 | data/infosys-ar-25.pdf
    Score: 0.666 | data/infosys-ar-25.pdf
    Score: 0.647 | data/infosys-ar-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'Performance Overview of Infosys report'
    [1] data/infosys-ar-25.pdf (Page 9)
    [2] data/infosys-ar-25.pdf (Page 9)
    [3] data/infosys-ar-25.pdf (Page 9)
    [4] data/infosys-ar-25.pdf (Page 9)
    [5] data/infosys-ar-25.pdf (Page 244)
  [Generate] Answer produced.

Assistant: The Infosys Integrated Annual Report 2024-25 provides a comprehensive overview of the company's performance and progress over the past year. Key highlights include:

- The report covers both quantitative and qualitative disclosures on material topics such as:
  - Financial performance
  - Environmental sustainability
  - Social responsibility
  - Relationship with stakeholders

- It also details Infosys' strategy, leadership commitment, and culture that emphasizes people, performance, and purpose.

- Infosys has a long-standing commitment to transparency and sustainability, having adopted the Global Reporting Initiative (GRI) principles 17 years ago and being the first IT company to publish sustainability performance according to the GRI G4 (comprehensive) criteria since 2014.

- The report is prepared in accordance with the International Integrated Reporting Framework, ensuring a holistic view of the company's value creation.

Regarding financial specifics from the year ended March 31, 2025:
- Cost of software packages and others increased to **₹9,617 million** from **₹6,891 million** in 2024.
- Other expenses were **₹3,497 million** in 2025 compared to **₹3,588 million** in 2024.
- Notable expense items include:
  - Power and fuel: **₹196 million** (2025) vs. **₹172 million** (2024)
  - Brand and marketing: **₹1,067 million** (2025) vs. **₹851 million** (2024)
  - Repairs and maintenance: **₹965 million** (2025) vs. **₹953 million** (2024)
  - Contributions towards Corporate Social Responsibility: **₹540 million** (2025) vs. **₹492 million** (2024)

Potential considerations:
- Increase in cost of software packages and third-party items for service delivery indicates higher investment or operational scale.
- Slight decrease in other expenses overall, despite increases in some categories.
- Continued focus on CSR and brand marketing reflects strategic priorities.

Sources:
- Infosys Integrated Annual Report 2024-25, Pages 16-17 (About the report)
- Infosys Integrated Annual Report 2024-25, Page 272 (Financial expenses details)

------------------------------------------------------------

You: an you provide Business highlights with key trends which contain revenue ,net profit etc from infosys report

Loading weights: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████| 199/199 [00:00<00:00, 7238.96it/s]
BertModel LOAD REPORT from: sentence-transformers/all-MiniLM-L12-v2
Key                     | Status     |  | 
------------------------+------------+--+-
embeddings.position_ids | UNEXPECTED |  | 

Notes:
- UNEXPECTED    :can be ignored when loading from different task/architecture; not ok if you expect identical arch.
    Score: 0.580 | data/infosys-ar-25.pdf
    Score: 0.580 | data/infosys-ar-25.pdf
    Score: 0.580 | data/infosys-ar-25.pdf
    Score: 0.580 | data/infosys-ar-25.pdf
    Score: 0.557 | data/infosys-ar-25.pdf
  [Retrieve] Found 5 relevant chunks for: 'an you provide Business highlights with key trends which contain revenue ,net profit etc from infosys report'
    [1] data/infosys-ar-25.pdf (Page 344)
    [2] data/infosys-ar-25.pdf (Page 344)
    [3] data/infosys-ar-25.pdf (Page 344)
    [4] data/infosys-ar-25.pdf (Page 344)
    [5] data/infosys-ar-25.pdf (Page 345)
  [Generate] Answer produced.

Assistant: The provided context from the Infosys Integrated Annual Report 2024-25 contains detailed segment-wise financial data but does not explicitly provide overall business highlights such as total revenue, net profit, or key trends in a summarized form.

However, based on the segment reporting data for the year ended March 31, 2025, here are some key financial figures:

| Segment                          | Revenue from Operations (₹ crore) | Segment Operating Income (₹ crore) |
|---------------------------------|----------------------------------|-----------------------------------|
| Financial Services               | **45,175**                       | **11,099**                        |
| Retail                          | **22,059**                       | **7,133**                         |
| Communication                   | **19,108**                       | **3,341**                         |
| Energy, Utilities, Resources & Services | **21,710**               | **6,097**                         |
| Manufacturing                   | **25,207**                       | **4,856**                         |
| Hi-Tech                        | **13,090**                       | **3,220**                         |
| Life Sciences                  | **11,831**                       | **2,663**                         |
| All other segments             | **4,810**                        | **827**                          |
| **Total**                      | **1,62,990**                     | **39,236**                       |

- The total revenue from operations across all segments is **₹1,62,990 crore** for the year ended March 31, 2025.
- The total segment operating income is **₹39,236 crore**.
- Unallocable expenses amount to **₹4,812 crore**.

Unfortunately, the context does not provide net profit figures or a narrative on key trends such as growth rates, margin changes, or strategic highlights.

Potential risks or assumptions:
- The data is segmented and does not include consolidated net profit or overall margin.
- No trend analysis or comparison with previous years beyond revenue and operating income is provided.
- Unallocable expenses are significant and should be considered when analyzing profitability.

For a comprehensive business highlight including net profit and key trends, additional sections of the report would be needed.

Sources:
- Infosys Integrated Annual Report 2024-25, Pages 372-373 (Segment reporting and financial data)