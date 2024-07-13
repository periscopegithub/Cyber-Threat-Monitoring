
## Cyber Threat Monitoring System

This notebook contains the complete code for the Cyber Threat Monitoring System of the Hong Kong Corporate Cybersecurity Platform. The system is designed to keep the threat database current by periodically scraping tweets from the Twitter (now X.com) profile of DeXpose (@dexpose_io2). This enables the platform to gather real-time data on recent vulnerabilities and cyber-attacks, ensuring timely and accurate cybersecurity insights for users.

### Environment
- Python 3.10.14
- Jupyter Notebook

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/periscopegithub/Cyber-Threat-Monitoring.git
    cd Cyber-Threat-Monitoring
    ```

2. Create a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

### Requirements

#### 1. API Keys
This project utilizes Azure's OpenAI API. You need to create a `.env` file in the root directory and add your API keys:

```
AZURE_OPENAI_ENDPOINT=your_endpoint_here
AZURE_OPENAI_KEY=your_key_here
AZURE_OPENAI_VERSION=your_version_here
AZURE_OPENAI_DEPLOYMENT_GPT35TURBO=your_gpt35turbo_deployment_here
AZURE_OPENAI_DEPLOYMENT_GPT4=your_gpt4_deployment_here
AZURE_OPENAI_DEPLOYMENT_GPT4O=your_gpt4o_deployment_here
AZURE_OPENAI_EMBEDDING_MODEL=your_embedding_model_here
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your_embedding_deployment_here

```

#### 2. Ollama
The scripts utilize Ollama for running local LLM. You need to install Ollama. Refer to the [Ollama website](https://ollama.com/) for installation instructions.

#### 3. Llama3 Model
Download the Llama3 model in Ollama for local LLM operations.

#### 4. CUDA and cuDNN
It is advised you have an Nvidia GPU with CUDA toolkit and cuDNN installed. Refer to the official [Nvidia CUDA](https://developer.nvidia.com/cuda-toolkit) and [cuDNN](https://developer.nvidia.com/cudnn) websites for installation instructions.

### References
- [DeXpose Twitter Profile](https://x.com/dexpose_io)
- ntscraper: https://github.com/bocchilorenzo/ntscraper

