# Chatbot Quickstart Guide

## Invoke a simple Open AI Chat Completion Endpoint

Here is a sample step-by-step guide to set up a simple Open AI chat endpoint so that you can experiment . Note that this guide is NOT meant to be used for any experimentation that will involve private data. Please only use this for testing with interactions that do not contain proprietary information or anything that should be kept secure.

1. Install jupyter notebook ([sample guide for MacOS](https://www.geeksforgeeks.org/how-to-install-jupyter-notebook-on-macos/))
2. Follow this [Jupyter notebook guide](https://www.youtube.com/watch?v=5pf0_bpNbkw) to get started with using it.
    - **Note:** To close a notebook, close the browser and then type `ctrl+c` in the terminal where the notebook is open.
3. Obtain Open AI API key by signing up on their [developer portal](https://openai.com/index/openai-api/). You will be charged on end-point usage based on the model you are invoking and volume of usage.
4. Set up your API key using this detailed [walkthrough from OpenAI](https://platform.openai.com/docs/quickstart/step-2-setup-your-api-key), or quickly just follow these steps:
    - In your mac terminal: `echo "export OPENAI_API_KEY='YOUR-API-KEY-HERE'" >> ~/.bash_profile` , hit enter
    - In terminal again: `source ~/.bash_profile` , hit enter
    - After doing the above steps and re-start the jupyter notebook, otherwise python won't register the change.
5. Install OpenAI on Jupyter by open a new cell on a notebook and type `!pip install --upgrade openai`. Leave this cell untouched when installation is done
6. [Open AI quickstarter](https://platform.openai.com/docs/quickstart/step-3-sending-your-first-api-request) and play around with the user prompt: `"Compose a poem that explains the concept of recursion in programming."`
7. For multi-line prompting, use triple-double quotes to enclose. For example, see the following code snippet, which enables you to replace the user prompt with the PROMPT variable.
```python
document = "JEE is an unnecessarily difficult engineering entrance exam that gives Indian kids nightmares"
PROMPT = """
Answer the following question using the given context:
What is JEE?

CONTEXT:
{context}""".format(context = document)
```
