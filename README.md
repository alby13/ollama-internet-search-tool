# Ollama Internet Search Tool
[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/downloads/)

Ollama AI Internet Search Tool for Local AI. A Python program that uses DuckDuckGo search results and AI response.

This program uses duckduckgo-search 6.2.6 https://pypi.org/project/duckduckgo-search/ to search the internet.

This program uses https://github.com/ollama/ollama-python Ollama Python library

## Explanation of the AI Integration with Web Search
The AI integration with the web search library works as follows:

User Query Processing:

The user inputs a query, which is then processed and cleaned (e.g., removing extra spaces, converting to lowercase).
Internet Search:

The query is passed to the search_internet function, which uses the duckduckgo_search library to perform a web search.
The DDGS class is instantiated to perform the search.
The text method is called with the user's query to get search results.
The results are filtered to ensure only those with a body field (containing the snippet) are kept.
Combining Search Results:

The search results are concatenated into a single string (search_content) that contains the snippets from each search result.
AI Response Generation:

The concatenated search content is passed along with the user's original query to the AI model via the ollama.chat method.
The AI model (e.g., llama3.1) processes both the user's query and the search results.
The AI model generates a response that integrates the information from the search results to provide a comprehensive answer to the user's query.
Returning the AI Response:

The AI-generated response is returned and printed.
The intended final behavior is that when the user asks the AI for information requiring an internet search, the AI uses this program to perform the search, integrates the results, and generates a response based on those results.

# How to use:

1. Install Required Libraries
First, install both ollama and duckduckgo-search libraries:

bash
<code>pip install ollama duckduckgo-search</code>

run
<code>python3 ddgsearch.py</code>
