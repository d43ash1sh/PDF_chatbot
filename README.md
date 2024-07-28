# PDF Assistant Bot 🤖

This project is a PDF Assistant Bot built using Streamlit, SpaCy, LangChain, and other libraries. The bot allows users to upload PDF files and ask questions based on the content of these files. It uses a retrieval-augmented generation (RAG) approach to provide answers.

## Features

- Upload multiple PDF files.
- Ask questions based on the content of the uploaded PDF files.
- Utilizes SpaCy for text embeddings and LangChain for managing the conversational chain.
- Integration with OpenAI's GPT-3.5 for generating responses.
- Easy-to-use Streamlit interface.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/d43ash1sh/PDF_chatbot
   cd pdf-assistant-bot
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # On Windows use `.venv\Scripts\activate`
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file and add your OpenAI API key:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   ```

## Usage

1. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

2. Once the app is running, you can upload your PDF files and start asking questions based on the content of these files.

## Project Structure

```bash
pdf-assistant-bot/
│
├── .env
├── .gitignore
├── app.py
├── requirements.txt
└── README.md
```

## Overview

### app.py

This is the main file of the project that contains all the code for the PDF Assistant Bot.

### Libraries Used:

- **streamlit**: For building the web interface.
- **PyPDF2**: For reading PDF files.
- **langchain**: For managing the conversational chain and embeddings.
- **dotenv**: For loading environment variables.
- **spacy**: For text embeddings.
- **os**: For handling file paths and environment variables.

### Functions:

- `pdf_read(pdf_doc)`: Reads and extracts text from uploaded PDF files.
- `get_chunks(text)`: Splits the extracted text into chunks.
- `vector_store(text_chunks)`: Stores the text chunks in a vector store using FAISS.
- `get_conversational_chain(tools, ques)`: Manages the conversational chain using LangChain and OpenAI's GPT-3.5.
- `user_input(user_question)`: Processes the user's input question.
- `main()`: The main function that sets up the Streamlit app interface.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, feel free to open an issue or create a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements

- Streamlit
- SpaCy
- OpenAI
- LangChain
- PyPDF2
