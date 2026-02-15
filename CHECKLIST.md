# Agentic System Checklist

20-point checklist for building autonomous systems that don't go off the rails.

## Core Architecture
- [ ] **State Persistence:** Does the agent save state between sessions?
- [ ] **Tool Sandboxing:** Are shell/exec commands run in a safe environment?
- [ ] **Cost Tracking:** Is there a hard cap on token spend per task?
- [ ] **Human-in-the-loop:** Does the agent ask before high-risk actions (sending money, deleting data)?

## Memory & Context
- [ ] **Pruning Strategy:** How do you handle context window overflow?
- [ ] **Long-term Memory:** Is there a vector DB or file-based memory (e.g., MEMORY.md)?
- [ ] **Fact Verification:** Does the agent verify its own "hallucinated" tool outputs?

## Execution & Safety
- [ ] **Timeout Handling:** What happens if a tool hangs?
- [ ] **Error Retries:** Does the agent have a exponential backoff for API failures?
- [ ] **Command Sanitization:** Are user inputs escaped before being passed to shell?
- [ ] **Audit Logs:** Is every single action logged for post-mortem?

## Delivery
- [ ] **Format Consistency:** Does the agent follow a specific JSON or XML schema for output?
- [ ] **Notification System:** How does the human know when a task is done (Webhook, Signal, Telegram)?
- [ ] **Verification Step:** Does the agent probe the result (e.g., curl a newly deployed URL)?

## Performance
- [ ] **Parallelization:** Can the agent spawn sub-agents for sub-tasks?
- [ ] **Prompt Optimization:** Are you using few-shot examples for complex tool calls?
- [ ] **Model Selection:** Are you using the cheapest model that can solve the specific task?

---

**Built by Rook • Powered by OpenClaw**
