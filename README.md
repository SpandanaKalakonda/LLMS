# LLMS

AI-Powered Document Retrieval and Question Routing System

Developed an AI-based system that routes user queries to the correct data source (vectorstore or Wikipedia) based on the nature of the question, enabling efficient and accurate information retrieval.
Data Ingestion and Document Processing:
Ingested and indexed web documents using LangChain and WebBaseLoader, processing over 67 documents.
Preprocessed and split documents into smaller chunks for efficient retrieval using RecursiveCharacterTextSplitter and Tiktoken.

Vector Database Management:
Deployed Cassandra as the vector store to store document embeddings created using HuggingFace's all-MiniLM-L6-v2 model.
Integrated the vectorstore with LangChain to enable fast and scalable document retrieval for machine learning algorithms.

Machine Learning Data Integration:
Leveraged HuggingFace embeddings to represent text and built a vector-based search for querying relevant machine learning content.
Developed a retrieval-augmented generation (RAG) system that retrieves documents based on user questions, reducing response time and increasing information accuracy.

Model Routing & Decision Logic:
Built a query routing logic using LangChain's ChatGroq to determine whether a question should be answered using a vectorstore (for machine learning content) or Wikipedia (for general information).
Used structured LLMs (Large Language Models) to categorize user queries and route them to the appropriate retrieval method, optimizing query responses.

Real-time API Integration:
Connected with WikipediaAPI to fetch and process the most relevant answers when the vectorstore is insufficient, ensuring comprehensive information coverage.
