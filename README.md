# Vibe Docing

> **The framework and manifesto for vibe docing: using AI to turn code, chats, and system artefacts into aligned, reviewable documentation.**

## What is Vibe Docing?

**Vibe docing** is the practice of using generative AI and natural language prompts to create, maintain, and structure documentation around real implementation evidence. It turns repositories, schemas, prompts, and system behaviour into working documentation that people and future agents can actually review.

While **vibe coding** allows developers to build fully functioning applications entirely through conversation, it introduces a massive risk: complex, black-box codebases that nobody actually understands. **Vibe docing** closes this gap. It uses AI-to-AI workflows to read generated systems and translate them back into clean, structured, and auditable artefacts.

---

## The Vibe Docing Workflow

Vibe docing flips traditional technical writing on its head by turning documentation into a conversational feedback loop grounded in source material:

### 1. The Context Dump
Instead of writing specifications from scratch, you hand your raw repository files, database schemas, or LLM chat history back to the AI.
* **The Prompt:** *"Read this repository I just vibe coded. Analyze the file structure and give me a high-level overview of how the main components, data flows, and responsibilities fit together."*

### 2. Conversational Refinement
You audit the AI's understanding and correct any false assumptions using plain, everyday language.
* **The Prompt:** *"That is mostly correct, but please document that changes only become permanent after an explicit confirmation step, not during intermediate edits. Add a dedicated troubleshooting section for synchronisation and state-handling issues."*

### 3. Automated Manifest Generation
The AI generates production-ready markdown files—such as a comprehensive `README.md` or a system-level `AGENTS.md`—which are committed directly back into the root of your project directory. The result should be living documentation, not a one-off summary.

---

## Why Vibe Docing is Mandatory

* **AI Agent Context Windows:** Future AI assistants cannot reliably modify or scale your application if they do not have a blueprint. Vibe docing creates the explicit context maps that future prompt cycles require.
* **Traceability & Review:** Good documentation should make it obvious what came from the source material, what is interpreted structure, and what is still assumption or intent.
* **Security & System Auditing:** Applications built entirely on "vibes" are highly prone to hidden logic flaws and security vulnerabilities. Vibe docing forces the AI to audit its own code and document the data boundaries.
* **Knowledge Retention:** When you return to an old project months down the road, you will not remember the prompt sequences or logic used to build it. Vibe docing preserves the foundational human intent, constraints, and operating model behind the code.

---

## The `AGENTS.md` Blueprint

The core output of a healthy vibe docing workflow is an `AGENTS.md` file placed at the root of your repository. This file serves as the working handoff for the next AI agent that opens your project.

### Recommended File Structure:
```markdown
# AI Agent Guide: Project Name

## System Architecture
[A high-level map of the codebase, tech stack, and state management]

## Source of Truth
[What is canonical, what is derived, and where evidence lives]

## Critical Logic & Edge Cases
[Crucial rules the AI must not break when modifying code]

## Environment & Secrets
[Required environment variables and local mock setups]

## Next Roadmap Goals
[The immediate next features intended for development]
```

---

## Origin & Contributing

This repository serves as the official, timestamped origin of the term **Vibe Docing**, coined by shane-pienaar-gbs.

If you have custom prompt templates, workflows, or ideas on how to build out the vibe docing framework, feel free to open an Issue or submit a Pull Request!
