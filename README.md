# Review Insights RAG (review-insights-rag-langchain)

**Review Insights RAG** is a project demonstrating a Retrieval-Augmented Generation (RAG) pipeline for extracting insights from product reviews. 
This pipeline uses [LangChain](https://github.com/langchain-ai/langchain) to combine context retrieval from a vector database with LLM-based question answering, enabling efficient and accurate analysis of textual data.

---

## Features

- **Data Loading**: Load product reviews from a CSV file.
- **Text Chunking**: Split documents into manageable chunks for vectorization.
- **Vector Store**: Build a Chroma vector database for efficient similarity-based retrieval.
- **Retrieval-Augmented QA**: Use the retrieved context to answer user questions with GPT-4o via LangChain.

---

## Usage

1. **Prepare your dataset:** Place your CSV file of reviews in the root directory. Update the `file_path` variable in the code if needed.
2. **Run the project:**
   - Open the `main.ipynb` file in your preferred Jupyter Notebook environment.
   - Execute the cells step by step to load the data, create embeddings, and run the RAG-based retrieval system.
4. **Modify behavior:**
   - Adjust the chunk size or overlap in the `CharacterTextSplitter` setup.
   - Update the `query` variable with your desired question.

---

## Example

**Input Query:**
```text
Based on the reviews in the context, tell me what people liked about the picture quality.
```

**Output:**
- **Retrieved Context:** Extracted relevant reviews about picture quality.
- **Answer:** Synthesized response based on the retrieved reviews.

---

## File Structure

```bash
📦 review-insights-rag-langchain
 ├── main.ipynb            # Core Jupyter Notebook containing the pipeline code
 └── tv-reviews.csv        # Example dataset of product reviews
```
