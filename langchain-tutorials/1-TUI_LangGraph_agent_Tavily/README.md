# #1 Python and Node.js TUIs for a LangGraph agent with a web connection

<br>

## 📖 Description 📖

Python and Node.js TUIs for a LangGraph ReAct agent using the [Tavily](https://tavily.com/) tool to get a web connection and an OpenAI LLM. The [ReAct](https://arxiv.org/abs/2210.03629) agent is able to decide on its own whether to use tools or not.

This directory has the following structure:

```
│   README.md
│
├───nodejs
│       node_modules
│       .env
│       .gitignore
│       package-lock.json
|       package.json
│       tui_langgraph_agent_tavily.js
│
└───python
        my-venv
        .env
        .gitignore
        requirements.txt
        tui_langgraph_agent_tavily.py
```

<br>

## 🚀 Installation 🚀

Before running [`tui_langgraph_agent_tavily.py`](https://github.com/rokbenko/ai-playground/blob/main/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/python/tui_langgraph_agent_tavily.py) or [`tui_langgraph_agent_tavily.js`](https://github.com/rokbenko/ai-playground/blob/main/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/nodejs/tui_langgraph_agent_tavily.js), follow these steps to start using TUIs.

> [!NOTE]
> The following instructions are specific to Windows. For macOS or Linux, please use the corresponding commands for your operating system.

### Python

1. Clone the repository: `git clone https://github.com/rokbenko/ai-playground.git`
2. Change the directory: `cd ai-playground/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/python`
3. Create an `.env` file to set up your environment variables
4. Create a virtual environment named `my-venv`: `python -m venv my-venv`
5. Activate the virtual environment `my-venv`: `my-venv\Scripts\activate`
6. Install the dependencies: `python -m pip install -r requirements.txt`
7. Run the Python script: `python tui_langgraph_agent_tavily.py`

> [!WARNING]
> Deactivate the virtual environment `my-venv` after you are finished by running the following command:
>
> ```
> deactivate
> ```

> [!IMPORTANT]
> Your `.env` file should contain the following environment variables:
>
> ```
> OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxx
> TAVILY_API_KEY=tvly-xxxxxxxxxxxxxxxxxxxxxxxxx
> ```

> [!TIP]
> You can verify that the virtual environment is created successfully if you see a folder named `my-venv` inside the `python` directory.
>
> ```
> │   README.md
> │
> ├───nodejs
> │       node_modules
> │       .env
> │       .gitignore
> │       package-lock.json
> |       package.json
> │       tui_langgraph_agent_tavily.js
> │
> └───python
>         my-venv 👈
>         .env
>         .gitignore
>         requirements.txt
>         tui_langgraph_agent_tavily.py
> ```
>
> You can verify that the virtual environment is activated successfully if you see `(my-venv)` at the beginning of your terminal prompt, like this:
> 
> ```
> (my-venv) C:\your\path\to\ai-playground\langchain-tutorials\1-TUI_LangGraph_agent_Tavily\python
> ```
>
> You can verify that the virtual environment is deactivated successfully if you *don't* see `(my-venv)` anymore at the beginning of your terminal prompt, like this:
>
> ```
> C:\your\path\to\ai-playground\langchain-tutorials\1-TUI_LangGraph_agent_Tavily\python
> ```

> [!NOTE]
> `venv` is a built-in Python module that allows you to create and manage virtual environments. If you have Python `v3.3` or higher installed, you can start using `venv` right away.

### Node.js

1. Clone the repository: `git clone https://github.com/rokbenko/ai-playground.git`
2. Change the directory: `cd ai-playground/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/nodejs`
3. Install the dependencies: `npm i`
4. Create an `.env` file to set up your environment variables
5. Run the Node.js script: `node tui_langgraph_agent_tavily.js`

> [!IMPORTANT]
> Your `.env` file should contain the following environment variables:
>
> ```
> OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxx
> TAVILY_API_KEY=tvly-xxxxxxxxxxxxxxxxxxxxxxxxx
> ```

<br>

## 🔥 Working example in Python 🔥

If you run [`tui_langgraph_agent_tavily.py`](https://github.com/rokbenko/ai-playground/blob/main/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/python/tui_langgraph_agent_tavily.py), you should be able to chat with the agent in a terminal:

> User:<br>
> Hi, I'm Bob.
> <br><br>
> Agent:<br>
> Hello Bob! How can I assist you today?
> <br><br>
> User:<br>
> What's the current weather in San Francisco? Give me exact data, like temperature, condition, wind, etc.
> <br><br>
> The agent is calling the tool 'tavily_search_results_json' with the query 'current weather in San Francisco'. Please wait for the agent's answer...
> <br><br>
> Agent:<br>
> The current weather in San Francisco is as follows:<br>
>
> - Temperature: 15.6°C (60.1°F)<br>
> - Condition: Sunny<br>
> - Wind: 6.9 mph, coming from NNW direction<br>
> - Pressure: 1013.0 mb<br>
> - Humidity: 83%<br>
> - Visibility: 16.0km (9.0 miles)<br>
> - UV Index: 4.0<br>
> - Cloud Cover: 0%<br>
> - Feels Like: 15.6°C (60.1°F)<br>
> - Wind Chill: 12.3°C (54.1°F)<br>
> - Heat Index: 13.0°C (55.4°F)<br>
> - Dewpoint: 9.1°C (48.3°F)<br>
> - Gust: 8.2 mph
> <br>
> For more details, you can visit [WeatherAPI.com](https://www.weatherapi.com/)
> <br><br>
> User:<br>
> Quit
> <br><br>
> Agent:<br>
> Have a nice day! 👋

### ⚒️ Tech stack ⚒️

OS:

- Windows `10`

Dependencies:

- [Python](https://www.python.org/) `3.11.8`
- [LangChain Python SDK](https://pypi.org/project/langchain/) `0.2.5`
- [LangChain Core Python SDK](https://pypi.org/project/langchain-core/) `0.2.9`
- [LangChain Community Python SDK](https://pypi.org/project/langchain-community/) `0.2.5`
- [LangChain OpenAI Python SDK](https://pypi.org/project/langchain-openai/) `0.1.9`
- [LangGraph Python SDK](https://pypi.org/project/langgraph/) `0.1.1`
- [Rich](https://pypi.org/project/rich/) `13.7.1`

<br>

## 🔥 Working example in Node.js 🔥

If you run [`tui_langgraph_agent_tavily.js`](https://github.com/rokbenko/ai-playground/blob/main/langchain-tutorials/1-TUI_LangGraph_agent_Tavily/nodejs/tui_langgraph_agent_tavily.js), you should be able to chat with the agent in a terminal:

> User:<br>
> Hi, I'm Bob.
> <br><br>
> Agent:<br>
> Hello Bob! How can I assist you today?
> <br><br>
> User:<br>
> What's the current weather in San Francisco? Give me exact data, like temperature, condition, wind, etc.
> <br><br>
> The agent is calling the tool 'tavily_search_results_json' with the query 'current weather in San Francisco'. Please wait for the agent's answer...
> <br><br>
> Agent:<br>
> The current weather in San Francisco is as follows:<br>
>
> - Temperature: 15.6°C (60.1°F)<br>
> - Condition: Sunny<br>
> - Wind: 6.9 mph, coming from NNW direction<br>
> - Pressure: 1013.0 mb<br>
> - Humidity: 83%<br>
> - Visibility: 16.0km (9.0 miles)<br>
> - UV Index: 4.0<br>
> - Cloud Cover: 0%<br>
> - Feels Like: 15.6°C (60.1°F)<br>
> - Wind Chill: 12.3°C (54.1°F)<br>
> - Heat Index: 13.0°C (55.4°F)<br>
> - Dewpoint: 9.1°C (48.3°F)<br>
> - Gust: 8.2 mph
> <br>
> For more details, you can visit [WeatherAPI.com](https://www.weatherapi.com/)
> <br><br>
> User:<br>
> Quit
> <br><br>
> Agent:<br>
> Have a nice day!

### ⚒️ Tech stack ⚒️

OS:

- Windows `10`

Dependencies:

- [Node.js](https://nodejs.org/en) `21.2.0`
- [LangChain Node.js SDK](https://www.npmjs.com/package/langchain) `0.2.7`
- [LangChain Core Node.js SDK](https://www.npmjs.com/package/@langchain/core) `0.2.10`
- [LangChain Community Node.js SDK](https://www.npmjs.com/package/@langchain/community) `0.2.14`
- [LangChain OpenAI Node.js SDK](https://www.npmjs.com/package/@langchain/openai) `0.2.1`
- [LangGraph Node.js SDK](https://www.npmjs.com/package/@langchain/langgraph) `0.0.25`
- [Terminal Kit](https://www.npmjs.com/package/terminal-kit) `3.1.1`

<br>

## 📽️ Demonstration 📽️

Coming soon... ✨
