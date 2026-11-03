In this project, you will explore large language models (LLMs) and agentic AI by designing, implementing, and evaluating an LLM-powered agent. You will use a locally hosted LLM (e.g., Llama through Ollama) so that the system can run without relying on external LLM APIs. The project will progress from interacting with a basic LLM to building an agent capable of using external tools, making decisions, and completing multi-step data science tasks.

# Part I: Exploring LLM Capabilities
Begin by experimenting with a local LLM and investigating how its behavior changes across different tasks and prompting strategies. Design prompts for tasks such as question answering, summarization, reasoning, data interpretation, and code generation. Compare different prompt designs and examine the quality, consistency, and limitations of the generated responses.

Consider questions such as:

How does prompt design affect the quality of LLM responses?

How consistent are responses when the same or similar prompts are used multiple times?

What types of tasks does the LLM perform well or poorly?

When does the model produce incorrect, unsupported, or hallucinated information?

# Part II: From an LLM to an Agent
Extend the basic LLM into an agentic system. Unlike a standard chatbot that directly generates a response, your agent should be able to determine whether additional actions are needed, select appropriate tools, use those tools, observe their results, and then decide how to proceed.

Your agent should follow a workflow similar to:

User Request → LLM Reasoning/Decision → Tool Selection → Tool Execution → Observation → Further Action or Final Response

Implement at least two tools that extend the capabilities of the LLM. Possible tools include:

Data Analysis Tool: use Python/Pandas to query, aggregate, or analyze a dataset.

Visualization Tool: generate appropriate charts based on user requests.

Statistical Tool: perform statistical tests or numerical calculations.

Database Tool: query structured data using SQL.

Retrieval Tool: retrieve relevant information from documents or a local knowledge base.

Machine Learning Tool: invoke a previously trained model to make predictions.

Your agent should decide when a tool is necessary, which tool to use, and what information to provide to that tool, rather than requiring the user to explicitly select the tool.

# Part III: Build a Data Science Agent
Design your agent around a meaningful data science application. You may use a dataset from a previous assignment or select another appropriate dataset.

Example projects include:

Flight Data Analyst Agent: A user may ask, “Which airlines experienced the highest delay rates during summer 2025?” The agent should recognize that the question requires data analysis, use the appropriate data tool to calculate the answer from the flight dataset, and provide an evidence-based response. It may also generate a visualization when requested.

Housing Analysis Agent: A user may ask questions about housing characteristics, prices, or neighborhoods. The agent can analyze housing data, invoke a trained housing-price prediction model, and explain the resulting prediction.

Dataset Exploration Agent: A user uploads or selects a dataset and asks questions such as “What are the major data-quality problems?”, “Which variables are most strongly related?”, or “Show me the most important trends.” The agent should select and execute appropriate analysis and visualization tools.

Your agent should support multiple types of user requests and demonstrate meaningful tool use rather than simply forwarding every question to the LLM.

# Part IV: Agent Evaluation
A working demonstration alone is not sufficient. You must systematically evaluate how reliably your agent performs.

Create at least 10 test tasks/questions that represent different levels and types of difficulty. Your test set should include:

Questions that the LLM can answer directly.

Questions that require one tool.

Questions that require multiple steps or tools.

Questions where the agent must choose between different tools.

Questions that may expose limitations or failure cases.

For each test case, record the expected behavior, tools selected, actual result, and whether the task was successfully completed.

Evaluate the agent from multiple perspectives, such as:

Answer Correctness: Is the final answer correct and supported by the available information?

Tool Selection: Did the agent select the appropriate tool?

Tool Execution: Did it provide appropriate inputs and correctly use the tool results?

Task Completion: Did the agent successfully complete the requested task?

Hallucination: Did the agent generate unsupported information rather than relying on tool results?

Robustness: How does the agent respond to ambiguous, unusual, or difficult requests?

Analyze representative successful and failed cases and explain why they occurred.

# Part V: Reflection
Based on your experiments, discuss the differences between a standalone LLM and an LLM-powered agent. Explain how tool use changes what an LLM-based system can accomplish and identify the major challenges you observed in building reliable agentic systems.

Your discussion should address questions such as:

What can your agent accomplish that the original LLM cannot?

When does the agent decide to use tools correctly or incorrectly?

Does adding tools always improve the quality of the response?

What are the major sources of failure?

What changes would make your agent more reliable?

Deliverables
Submit a reproducible Jupyter Notebook or Python project containing your implementation, prompts, agent workflow, tool definitions, experiments, evaluation results, and discussion. Include a simple diagram illustrating your agent architecture and a table summarizing your test cases and evaluation results.

Your final project should demonstrate the complete progression:

LLM → Prompting → Tool Use → Agentic Workflow → Data Science Tasks → Systematic Evaluation → Failure Analysis

The goal of this assignment is not simply to build a chatbot, but to understand how LLMs can be transformed into agents that reason about tasks, interact with tools, and perform useful data science operations—and how such systems should be systematically evaluated for reliability and limitations.