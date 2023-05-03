# langchain-ask-pdf

Features

Autoload the PDF in file file

The BytesIO and PdfReader classes from the PyPDF2 library are imported to handle the PDF file.
The CharacterTextSplitter, OpenAIEmbeddings, FAISS, load_qa_chain, OpenAI, and get_openai_callback classes are imported from the langchain library. These classes are used to build the question-answering system.
The OpenAI API key is set as an environment variable using the os module.
The st.set_page_config and st.header functions from the streamlit library are used to set the title and header of the web app.
The PDF file is loaded using the open function and read in binary mode using the rb flag. The contents of the file are then stored in a BytesIO object.
The text content of the PDF file is extracted using the extract_text method of the PdfReader class. The text is concatenated into a single string.
The CharacterTextSplitter class is used to split the text into smaller chunks. These chunks are used to build a knowledge base for the question-answering system.
The OpenAIEmbeddings class is used to generate embeddings for the text chunks. These embeddings are used to perform similarity searches when answering questions.
The st.text_input function is used to prompt the user to ask a question about the PDF file.
If the user enters a question, the similarity search is performed using the knowledge_base.similarity_search method. The resulting documents are passed to the load_qa_chain function to create a question-answering chain.
The run method of the question-answering chain is called with the input documents and user question as arguments. The result is stored in the response variable.
The result is displayed using the st.write function.
Overall, the code creates a simple web app that allows users to ask questions about a PDF document and receive answers based on the content of the document. The app uses the langchain library to build a question-answering system that leverages the OpenAI API for natural language processing.

### We keep the feature that calculate the cost 

![image](https://user-images.githubusercontent.com/17680194/236060286-6b796e29-359c-436e-b9a9-2c8553920914.png)

