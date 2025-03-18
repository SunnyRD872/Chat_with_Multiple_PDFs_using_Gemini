
# Chat with Multiple PDFs using Gemini

This Streamlit application allows users to upload multiple PDF files, process them, and interact with the content using Google's Gemini model. Users can ask questions about the uploaded PDFs, and the application will provide detailed answers based on the content of the documents.


## Features

- **Multi-PDF Support**: Upload and process multiple PDF files simultaneously.

- **Text Extraction**: Efficiently extract text from PDFs, including handling complex layouts.

- **Intelligent Text Chunking**: Split text into manageable chunks for optimal processing.

- **Vector Embeddings**: Use Google's Gemini embeddings for high-dimensional text representation.

- **FAISS Vector Store**: Leverage FAISS for fast and scalable similarity search.

- **Conversational AI**: Interact with your documents using Google's Gemini model for accurate, context-aware answers.

- **Customizable Prompts**: Tailor AI responses with a customizable prompt template.

- **User-Friendly Interface**: A clean and intuitive Streamlit interface for seamless interaction.

- **Local Storage of Vector Index**: Save and reuse the FAISS vector index for faster processing.

## Prerequisites

Before running the application, ensure you have the following installed:

- Python 3.7 or higher(Used python version- 3.12.7)

- Streamlit

- PyPDF

- LangChain

- Google Generative AI

- FAISS

- python-dotenv

- You can install the required packages using pip:

pip install streamlit pypdf langchain langchain-google-genai faiss-cpu python-dotenv

## Setup

- Google API Key: Obtain a Google API key from the **suitemaker.google**. Ensure that the API key has access to the Gemini model.

- Environment Variables: Create a .env file in the root directory of your project and add your Google API key

  google_api_key=your_google_api_key_here

- Running the Application: Navigate to the project directory and run the Streamlit application:

     streamlit run app.py
## Usage

1.**Upload PDFs**: Use the sidebar to upload one or more PDF files. Click the "Submit and Process" button to extract and process the text from the PDFs.

2.**Ask Questions**: Once the PDFs are processed, you can ask questions in the main input box. The application will provide answers based on the content of the uploaded PDFs.
## Code Structure

- **get_pdf_text(pdf_docs)**: Extracts text from the uploaded PDF files.

- **get_text_chunks(text)**: Splits the extracted text into chunks for processing.

- **get_vector_store(text_chunks)**: Creates and stores FAISS vector embeddings of the text chunks.

- **get_conversational_chain()**: Sets up the conversational chain with a custom prompt template.

- **user_input(user_question)**: Handles user questions and generates responses using the conversational chain.

- **main()**: The main function that sets up the Streamlit application and handles user interactions.


## Screenshots
Screenshot of Streamlit Userface Interface:
![App Screenshot](https://imgur.com/J8aVPWk.png)


## Acknowledgements

This project was inspired by and learned from [Krish Naik](https://youtu.be/uus5eLz6smA?si=vG6HR41Y6WVmsSCc). Special thanks to him for his excellent tutorials and guidance on building AI-powered applications.

Additionally, this project leverages the following tools and frameworks:

 - [suitemaker](https://www.google.com/search?q=suitemaker.google&oq=&gs_lcrp=EgZjaHJvbWUqCQgBECMYJxjqAjIJCAAQIxgnGOoCMgkIARAjGCcY6gIyDwgCEC4YJxjHARjqAhjRAzIJCAMQIxgnGOoCMgkIBBAjGCcY6gIyCQgFECMYJxjqAjIJCAYQIxgnGOoCMgkIBxAuGCcY6gLSAQoxNDgxNzdqMGo3qAIIsAIB8QV9we58A9O5ovEFfcHufAPTuaI&sourceid=chrome&ie=UTF-8) for Google API Key.

 - [Streamlit](https://streamlit.io/) for the web application framework.

 - [langchain](https://www.langchain.com/) for the conversational chain and text processing utilities.
 - [FAISS](https://github.com/facebookresearch/faiss) for efficient similarity search and clustering of dense vectors.

Special thanks to the developers and communities behind these amazing tools for making this project possible!
 

