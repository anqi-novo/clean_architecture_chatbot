# Clean Architecture Chatbot

## Prerequisites

- Python 3.9+
- Docker

## Get an OpenAI API Key

You need to deploy your own model with Azure OpenAI services and obtain the key, deployment name, etc.

### Secrets

1. Create a `.streamlit` folder in the root directory.
2. Add a `secrets.toml` file to it with the following data:

```toml
# .streamlit/secrets.toml
AZURE_OPENAI_ENDPOINT = "<endpoint>"
AZURE_OPENAI_KEY = "<api_key>"
AZURE_OPENAI_API_VERSION = "<version>"  # for example, "2023-05-15"
AZURE_OPENAI_CHATGPT_DEPLOYMENT = "<deployment>"
EMBEDDINGS_MODEL = "<model_name>"
```

### Running the App from Docker

1. **Build the Docker Image**:
   If you don't have Docker installed, download and install it from the official Docker website. Then build the Docker image using the provided Dockerfile.

   ```bash
   docker build -t chatbot-app .
   ```

2. **Run the Docker Container**:
   Start the Docker container running your Streamlit app using the following command:

   ```bash
   docker run -p 8501:8501 chatbot-app
   ```

3. **Access the Streamlit App**:
   Once the container is running, you can access your Streamlit web application by opening a web browser and navigating to `http://localhost:8501`.

### Running the App on Your Machine

1. **Create a Virtual Environment**:
   Create a new Python virtual environment to isolate the dependencies required for the app.

   ```bash
   python -m venv myenv
   ```

2. **Activate the Virtual Environment**:
   Activate the virtual environment before installing the required packages and running the app.
   
   - On Windows:
     ```bash
     myenv\Scripts\activate
     ```
   
   - On macOS and Linux:
     ```bash
     source myenv/bin/activate
     ```

3. **Install Required Packages**:
   Install the necessary packages specified in the `requirements.txt` file.

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the App**:
   Run the Streamlit app using the following command:

   ```bash
   streamlit run app.py
   ```

5. **Access the Streamlit App**:
   After running the app, you should be able to access it by opening a web browser and navigating to `http://localhost:8501`.

With these steps completed, users will be able to run the Streamlit app either using Docker or directly on their own machine.

