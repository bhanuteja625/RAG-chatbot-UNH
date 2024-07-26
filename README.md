# RAG-chatbot-UNH
RAG-chatbot-UNH is a chatbot designed to assist students at the University of New Haven by providing accurate answers to their inquiries. The bot utilizes a large language model (LangChain) and a vector database (Pinecone) to deliver precise responses.

## Features
*  Natural Language Understanding: Leverages LangChain for understanding and generating human-like responses.
*  Vector Search: Uses Pinecone to efficiently search through a knowledge base of FAQs.
*  Web Interface: A user-friendly Flask web application for interactions.

## Installation
  Prerequisites
  * Python 3.8+
  * MongoDB
  * Pinecone account
  * OpenAI API key
  * A `.env` file with necessary environment variables

## Setup Instructions
1. Environment Variables
Create a .env file with the following:

 ```
    PINECONE_API_KEY=your_pinecone_api_key
    PINECONE_ENVIRONMENT=your_pinecone_environment
    PINECONE_INDEX=your_pinecone_index_name
```
2. MongoDB Configuration
Set up a MongoDB database and collection for storing conversations.
Update the MongoDB URI in the main Flask app.py file.
3. Pinecone Configuration
Set up a Pinecone account and create an index.
Update your .env file with the Pinecone details.
4. Install Dependencies
Run the following command to install the necessary Python packages:
    pip install -r requirements.txt
   
## Running the Application
Data Loading
Optional: The data may already be loaded.

To load data:

    python loaddata.py
    
Starting the Flask App
To start the Flask server:

    python app.py
    
Alternatively, using Docker:

Build the image:

    docker build -t rag-chatbot-unh .
    
Run the container:

    docker run -p 5000:5000 rag-chatbot-unh
    
Accessing the Web Interface: 
Visit http://localhost:5000/ to interact with the chatbot.

## Usage
Users can ask questions via the chat interface.
The bot provides answers, including sources when available.
## Managing Data
Conversation data is stored in MongoDB. Use MongoDB tools for data management and analysis.

## Troubleshooting
Check the following if issues occur:

* Environment variables in .env.
* MongoDB URI and database accessibility.
* Pinecone index configuration and permissions.
* Validity of Pinecone and OpenAI API keys.


## Files and Directories
* app.py: Main Flask application.
* load_data.py: Script to load data into Pinecone.
* static/: Contains static files like CSS and images.
* templates/: HTML templates for the web app.
* requirements.txt: List of dependencies.



