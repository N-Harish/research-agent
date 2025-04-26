# research-agent
Given a topic to search, agent returns content by searching web and also cites the sources

## Steps to run
* Get Tavily API Key from [here](https://docs.tavily.com/documentation/api-reference/endpoint/search)
* Create a .env file and add the API Key as follows
  ```
  TAVILY_API_KEY=<your key>
  ```
* Download ollama from [here](https://ollama.com/download)
* Run ```ollama pull llama3.2``` to pull llama3.2 model
* Run ```pip3 install -r requirements.txt``` to install all the dependencies
* Now run ```streamlit run app.py``` to start the UI to search


## Agents Architecture used
There are two agents at play here (both are llama3.2 from ollama):
1. Researcher agent: this agent is a react agent (Reason and Act agent) which uses the Tavily search tool to gather information from internet on the given topic
2. Content Writer agent: This agent takes the content extracted by research agent and then writes an article (with citation) on the given topic

## Architechture

![Untitled Diagram](https://github.com/user-attachments/assets/d84a46ab-d06f-4a05-b5ba-86ccf4fdafaa)
