# Banking FAQ Chatbot

The chatbot utilizes the Zephyr-7B-Beta LLM for generating human-like, contextually relevant answers, ensuring smooth and dynamic interactions. To achieve this, the project employs LangChain for seamless language model integration and Chroma, a robust vector store, for efficient storage and retrieval of document embeddings. With domain-specific datasets, the chatbot is trained to understand and respond accurately to a wide range of banking queries.

## Project Overview

This chatbot leverages advanced machine learning techniques to provide quick and accurate answers to common banking queries. It uses LangChain for language model integration, Chroma as a vector store for persistent embeddings, and Hugging Face embeddings for natural language understanding.

## Features
- **Custom Query Handling**: Responds intelligently to user queries related to banking FAQs.
- **Persistent Vector Store**: Uses Chroma to store document embeddings for quick retrieval.
- **Zephyr-7B-Beta LLM**: Powered by large language models Used for generating human-like responses and handling context-aware interactions.
- **Domain-Specific Knowledge**: Incorporates finance-specific datasets to improve accuracy.

## Workflow

1. **Data Preparation**:
   - A CSV file containing banking FAQs and their answers is processed and converted into `LangChain` document objects.
   - Each document represents a single question-answer pair, including metadata for easy retrieval.

2. **Vectorization**:
   - Uses `HuggingFaceEmbeddings()` from `langchain_community.embeddings` to transform text data into vector representations.
   - These embeddings are stored persistently in Chroma, allowing efficient similarity-based searches.

3. **Model Integration**:
   - The chatbot is powered by the Zephyr-7B-Beta LLM, integrated via LangChain, offering context-aware and fluent natural language interactions.
   - The interaction flow is maintained with structured message types (System Message, Human Message, AI Message) to ensure a coherent and dynamic conversation flow.

4. **Query Processing**:
   - User inputs are vectorized and matched against stored embeddings in Chroma.
   - The closest matches are retrieved, and the LLM generates a contextually relevant response.

5. **Deployment**:
   - The project runs in a Jupyter Notebook with plans for Streamlit deployment for a user-friendly web interface.

## Models and Libraries Used
-**Zephyr-7B-Beta LLM**: 
  -Used for generating human-like responses and handling context-aware interactions.
- **Hugging Face Embeddings**:
  - Embedding Model: `HuggingFaceEmbeddings()` from `langchain_community.embeddings` for creating document embeddings.
- **LangChain**:
  - For building the chatbot pipeline and integrating OpenAI's GPT models.
- **Chroma Vector Store**:
  - For storing and retrieving vectorized embeddings.
