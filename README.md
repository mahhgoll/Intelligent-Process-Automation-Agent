# Organizational Process Analysis & Automation — Final Project

A simple multi-agent organizational process analysis system built with LangGraph.

## Architecture

RAG Agent → Diagnostic Agent → Process Engineer → Human Manager

If the manager provides feedback:

Human Manager → Process Engineer → Human Manager

If the manager approves:

Human Manager → END

## Main technologies

- Python
- LangGraph
- LangChain
- Gemini
- RAG
- FAISS Vectorstore
- Tool Calling
- Human-in-the-Loop
- Checkpointer / Interrupt / Command

## Scenarios

### Scenario 1 — VPN Access

The documented SLA is 2 hours, while the simulated actual average is 24 hours.
The main bottleneck is direct-manager approval.
The proposed automation uses organizational messaging for approval and then calls the firewall API.

### Scenario 2 — Sensitive Database Access

The first proposal attempts to remove security approval.
The human manager rejects this because security approval is mandatory.
The graph returns to the Process Engineer, which creates a revised solution that keeps security approval and speeds up the review, for example with a dashboard/queue for the security officer.

## Files

- `Mahboobeh_Final_Project.ipynb` — complete notebook
- `final_project_graph.png` — generated automatically after running the graph visualization cell

## Important

The API key is read from the Google Colab Secret named `GOOGLE_API_KEY`.
No API key is stored in the notebook.
