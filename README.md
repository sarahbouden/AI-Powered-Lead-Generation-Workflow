# 🤖 AI-Powered Lead Generation Workflow
## Project Overview 🎯
This project is an automated, multi-agent AI workflow built in n8n to streamline the process of lead generation from LinkedIn. The system intelligently identifies, enriches, and qualifies leads, transforming a traditionally manual task into an efficient, automated pipeline.

The core of the workflow leverages a series of specialized APIs and AI models to progressively enrich data, starting from a simple search query and ending with a comprehensive, sales-ready lead profile.


## The Workflow: How It Works ⚙️
The entire process is orchestrated as a sequence of connected nodes within n8n, where each step builds upon the last.


### 1.Lead Identification (Google Search API):

* The workflow begins by querying Google's Programmable Search Engine to find relevant LinkedIn profiles based on specific criteria (e.g., "Data Scientists in Berlin").

### 2.Information Extraction (Groq):

* The LinkedIn profile URLs are passed to a high-speed Groq AI model.

* This agent intelligently extracts key information from the search results, such as the person's full name, job title, and current company.

### 3.Company URL Enrichment (SerpApi):

* Using the extracted company name, SerpApi is called to perform a targeted search and find the official company website URL, ensuring data accuracy.

### 4.Contact Enrichment (Kaspr API):

* The person's name and company URL are fed into the Kaspr API, which specializes in finding and verifying professional email addresses and phone numbers.

### 5.Company Summarization (Relevance AI):

* Finally, the workflow uses a custom tool built with Relevance AI. This tool takes the company's URL and generates a concise summary of its business, providing valuable context for personalized outreach.

## Technology Stack & APIs 🛠️
* Orchestration Platform: n8n

* AI Language Model: Groq (for fast information extraction)

* Web Search: Google Custom Search API & SerpApi

* Contact Enrichment: Kaspr API

Custom AI Tooling: Relevance AI
