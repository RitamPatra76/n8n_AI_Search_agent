# n8n_AI_Search_agent

This repository showcases an AI agent I developed using n8n, a visual workflow automation tool. While I have built several AI agents in the past using frameworks like LangChain and LangGraph, this is my first project using n8n. I’ve always seen others sharing n8n-powered AI agents on LinkedIn and other platforms, and finally decided to give it a try. To my surprise, building the same kind of agent that usually takes me 2.5+ hours, took just 15 minutes in n8n. It’s truly that intuitive and developer-friendly.

# What This Agent Does
This AI agent is essentially a refined search assistant. Here's the problem it solves:

Traditional Google searches, even with the newer AI enhancements, tend to return long lists of links or fragmented pieces of information. Similarly, searching with tools like ChatGPT alone can lead to vague or insufficient responses when the LLM doesn’t have up-to-date knowledge.

This AI agent intelligently combines:

GPT-4o-mini for direct question-answering

Google Search (via SerpAPI) when real-time or external data is needed

The result? Clear, concise, and informative answers, without overwhelming the user or leaving out critical context.

# How the Workflow Works
Here’s a breakdown of how the agent functions (visualized in Workflow.jpg):

User sends a search query via chat, triggering the Chat Trigger node in n8n.

The question is first passed to GPT-4o-mini:

If GPT knows the answer (e.g., “What is the speed of light?”), it responds directly.

If GPT cannot answer confidently, it proceeds to the next step.

The query is sent to Google via SerpAPI.

The retrieved search results are then fed back into GPT, which summarizes and refines the output into a final answer.

It’s simple yet powerful — delivering intelligent responses that balance LLM reasoning and real-time information.

# Demo Example
To test the AI agent, I asked:

"What are the recent news on Iran-Israel conflict? Give me everything very briefly."

The output — a well-organized, informative summary, is shown in sample_output.jpg.

You can also watch the full demo and automation flow in demo_n8n_ai_search_agent.mp4.
