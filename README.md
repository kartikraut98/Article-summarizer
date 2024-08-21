# Article-summarizer

A user-friendly summarizer designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the stock market and financial domain.

## Description:
This Python script builds a Streamlit web application called "Article Summarizer." It allows users to input up to three news article URLs via a sidebar. Upon clicking "Process URLs," the script retrieves and processes the content of these URLs using the UnstructuredURLLoader, splitting the text into smaller chunks for better analysis. It then generates embeddings using OpenAI's API and stores them in a FAISS vector index, which is saved as a pickle file for later use. Users can input queries, and the tool retrieves relevant answers along with their sources by loading the saved FAISS index and leveraging a retrieval-based question-answering chain powered by OpenAI's language model.

## Features
Load URLs or upload text files containing URLs to fetch article content.<br>
Process article content through LangChain's UnstructuredURL Loader.<br>
Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information.<br>
Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.<br>


## Meta data:
main.py: The main Streamlit application script.<br>
requirements.txt: A list of required Python packages for the project.<br>
faiss_store_openai.pkl: A pickle file to store the FAISS index.<br>
.env: Configuration file for storing your OpenAI API key.<br>

## Installation
1. Clone this repository to your local machine using:<br>
    git clone https://github.com/kartikraut98/Article-summarizer.git<br>
2. Navigate to the project directory:<br>
3. Install the required dependencies using pip:<br>
    pip install -r requirements.txt<br>
4. Set up your OpenAI API key by creating a .env file in the project root and adding your API<br>
    OPENAI_API_KEY=your_api_key_here
