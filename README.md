
# AtifBot: Movie Explorer Tool 


## Features

- Load URLs or upload text files containing URLs to fetch movies content.
- Process movies or artilce content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.

### Option 1: Running Directly on Local Machine
## Installation

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/atif275/movie_explorer_tool_project.git
```
2.Navigate to the project directory:

```bash
  cd movie_explorer_tool_project
```
3. Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```
4.Set up your OpenAI API key by creating a .env file in the project root and adding your API

```bash
  OPENAI_API_KEY=your_api_key_here
```
## Usage/Examples

1. Run the Streamlit app by executing:
```bash
streamlit run main.py

```
### Option 2: Running on Docker 
## Installation

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/atif275/movie_explorer_tool_project.git
```
2.Navigate to the project directory:

```bash
  cd movie_explorer_tool_project
```
3. Build the Docker image (docker should be runnng on your machine):

```bash
  docker build -t atifbot-movie-explorer .
```
4. Run the Docker image:

```bash
  docker run -p 8501:8501 atifbot-movie-explorer

```
5. Navigate to:
```bash
  URL: http://0.0.0.0:8501
  You can now view your Streamlit app in your browser.

```


2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles

## Project Structure

- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai.pkl: A pickle file to store the FAISS index.
- .env: Configuration file for storing your OpenAI API key.