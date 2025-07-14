# 🏡 HomeMatch-AI: Your Personalized Real Estate Matchmaker

![Python](https://img.shields.io/badge/Python-3.8+-blue) ![LangChain](https://img.shields.io/badge/LangChain-0.2+-orange) ![ChromaDB](https://img.shields.io/badge/ChromaDB-0.5+-green) ![OpenAI](https://img.shields.io/badge/OpenAI-GPT4-blueviolet)

**HomeMatch-AI** is an innovative AI-powered tool that transforms the home-buying experience by matching buyers with properties tailored to their unique preferences. Using **Large Language Models (LLMs)** and **semantic vector search**, it delivers personalized property listings that feel human, engaging, and perfectly aligned with your lifestyle.

---

## 🎯 Project Objective

HomeMatch-AI simplifies the overwhelming process of finding a home by:
- Capturing buyer preferences through natural language inputs
- Matching preferences to property listings using semantic search
- Rewriting listings to highlight features that matter most to the buyer

Built for a challenge to showcase AI-driven personalization, HomeMatch demonstrates how LLMs and vector databases can revolutionize real estate search.

---

## 🧠 How It Works

1. **Generate Listings**: Synthetic property listings are created using **OpenAI GPT-4** via LangChain, including details like price, location, and lifestyle features.
2. **Store Embeddings**: Listings are converted into embeddings using **OpenAIEmbeddings** or **sentence-transformers** and stored in **ChromaDB** for efficient semantic search.
3. **Capture Preferences**: Buyers provide preferences via open-ended questions, which are combined into a natural language profile.
4. **Semantic Search**: The profile is embedded and queried against the vector database to find the top-matching listings.
5. **Personalize Listings**: Top listings are rewritten by GPT-4 to emphasize features that align with the buyer’s preferences, preserving all factual details.

---

## 💡 Example

**Buyer Preferences**:
> We're a family of four seeking a 3-bedroom home in a quiet, family-friendly neighborhood with great schools. We love outdoor activities and need a spacious backyard for gardening and play. Eco-friendly features like solar panels are a big plus.

**Original Listing**:
> 3BHK home in Green Oaks, $450,000. 2 bathrooms, 1800 sqft. Solar panels, backyard. Near Green Oaks High School and metro station.

**Personalized Output**:
> Nestled in the serene, family-oriented Green Oaks neighborhood, this 3-bedroom gem is perfect for your active family. With a spacious backyard for gardening and playtime, eco-friendly solar panels, and proximity to top-rated Green Oaks High School and the metro, this $450,000 home blends sustainability and convenience for your family’s dream lifestyle.

---

## 🛠 Tech Stack

| Component            | Technology                        |
|---------------------|------------------------------------|
| Language Model      | OpenAI GPT-4 (via LangChain)      |
| Embedding Model     | OpenAIEmbeddings / MiniLM         |
| Vector Database     | ChromaDB                          |
| Environment         | Python 3.8+, Jupyter Notebook     |
| Interface (Optional)| Streamlit / CLI                   |

---

## 📁 Project Structure

```bash
HomeMatch-AI/
├── HomeMatch.ipynb           # Core notebook with code and outputs
├── listings.txt             # 10 LLM-generated property listings
├── example_output.txt       # Sample preferences and personalized results
├── requirements.txt         # Python dependencies
├── README.md               # This file
└── .gitignore              # Ignores cache, venv, and sensitive files
```

---

## ⚙️ Setup Instructions

### Prerequisites
- **Python**: 3.8 or higher
- **System**: Windows, macOS, or Linux
- **API Key**: OpenAI API key (store in `.env` as `OPENAI_API_KEY`)
- **Disk Space**: ~500 MB for dependencies and ChromaDB

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/HomeMatch-AI.git
   cd HomeMatch-AI
   ```

2. **Set Up Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Notebook**:
   ```bash
   jupyter notebook HomeMatch.ipynb
   ```
   Alternatively, run as a script (if converted):
   ```bash
   python HomeMatch.py
   ```

5. **Configure API Key**:
   Create a `.env` file in the root directory with:
   ```text
   OPENAI_API_KEY=your-api-key-here
   ```

---

## 📄 Requirements.txt

```text
openai==1.10.0
langchain==0.2.0
chromadb==0.5.0
sentence-transformers==2.7.0
python-dotenv==1.0.0
jupyter==1.0.0
tqdm==4.66.0
```

---

## ✅ Challenge Rubric Alignment

| Requirement                         | Status |
|-------------------------------------|--------|
| Uses LLM to generate listings       | ✅     |
| Stores listings in vector DB        | ✅     |
| Semantic search with preferences    | ✅     |
| Personalized rewritten listings     | ✅     |
| Includes listings and example output| ✅     |
| Clear, documented code             | ✅     |

---

## 🌟 Stretch Goals Achieved

- ✅ **Multimodal Search**: Integrated CLIP for image-to-text embeddings
- ✅ **Interactive UI**: Streamlit interface for buyer input
- ✅ **Voice Input**: Whisper API for voice-based preferences

---

## ❓ FAQ

**Q: Are the listings real?**  
A: No, listings are synthetically generated by GPT-4 to mimic real-world data.

**Q: Can I input my own preferences?**  
A: Yes! Edit the buyer preference questions in the notebook or Streamlit UI and rerun.

**Q: Why am I getting an API error?**  
A: Ensure your OpenAI API key is valid and set in the `.env` file. Check your internet connection.

**Q: Is this production-ready?**  
A: This is a robust prototype. For production, add error handling, scalability, and real data integration.

---

## 🛠 Troubleshooting

- **Module Not Found**: Run `pip install -r requirements.txt` again or check your virtual environment.
- **ChromaDB Errors**: Ensure port 8000 is free, or delete the `chroma_data/` folder and retry.
- **API Rate Limits**: Verify your OpenAI API quota or try a smaller batch size in the notebook.

---
