---
name: ai-agent-workflow
description: "Use when designing or improving AI engineering workflows after the stack direction is already mostly known. Covers prompt pipelines, MCP integrations, tool-using agents, reusable skills, evaluation loops, and workflow decomposition. Trigger this for agent architecture, prompt refinement, tool grounding, workflow design, and turning repeatable AI tasks into durable systems. If the main question is local model selection, deployment path, or LM Studio versus Ollama versus MLX, use local-ai-systems-studio instead."
---

# AI Agent Workflow

Use this skill when the goal is not just to get one answer, but to build a repeatable AI-assisted workflow and the main stack direction is already mostly known.

This skill is for taking AI ideas and turning them into structured loops: prompts, tools, retrieval, checks, and reusable building blocks.

## Inputs

Useful inputs for this skill include:
- the repeatable task you want the workflow to handle
- current prompt, script, tool, or skill draft if one exists
- model constraints such as local-only or API limits when the basic stack is already chosen
- available tools, MCP servers, files, or data sources
- quality bar, failure modes, and evaluation expectations

## Outputs

Strong outputs from this skill usually include one or more of:
- a reusable workflow specification
- a prompt template or prompt stack
- a tool integration or MCP plan
- an evaluation loop or quality rubric
- a recommendation for whether this should be a prompt, skill, script, or MCP server
- a minimal implementation path with clear next steps

## Non-goals

This skill is not the best fit for:
- choosing between local deployment stacks such as MLX, GGUF, LM Studio, Ollama, or vLLM
- hardware-first local LLM decisions or local serving setup questions
- one-off content writing with no reusable workflow need
- generic code fixes unrelated to AI systems or tooling
- visual design, portfolio packaging, or office-document polish
- hand-wavy AI brainstorming that never needs an explicit operating loop

## Workflow

1. Define the unit of work.
Clarify what the workflow should repeatedly accomplish:
- generate
- transform
- evaluate
- retrieve
- route
- summarize
- orchestrate tools

2. Choose the right control surface.
Decide whether the problem is best solved by:
- better prompting
- a reusable skill
- MCP tool integration
- structured references
- evaluation and iteration
- a small script or automation

If the decision is still mainly about local stack choice, deployment path, or hardware fit, hand the problem to `local-ai-systems-studio` first.

3. Keep the workflow explicit.
Spell out:
- inputs
- steps
- tool calls
- expected outputs
- failure handling
- validation points

4. Design for iteration.
If quality matters, include a loop:
- draft
- inspect
- revise
- compare
- finalize

## Examples

### Example 1: Local LLM workflow design
User request:
> I want to use my local Qwen model to summarize PDFs, extract tasks, and save clean notes.

Good use of this skill:
- assume the local stack is already basically chosen
- separate extraction, cleanup, and summarization stages
- define what can stay prompt-only versus what should call tools
- specify stable input and output shapes so the workflow can be repeated

### Example 2: Skill or MCP decision
User request:
> Should this document-processing task become a skill, a script, or an MCP server?

Good use of this skill:
- compare control surfaces honestly
- optimize for reuse, tool access, and maintenance cost
- recommend the smallest durable abstraction that solves the real problem

### Example 3: Evaluation loop
User request:
> Help me build an eval loop for this agent so I can tell if the outputs are getting better.

Good use of this skill:
- define success criteria and failure categories
- design draft, review, revise, and compare steps
- suggest lightweight evaluation before overbuilding infrastructure

## Pairing With Other Skills

Use these when appropriate:
- `local-ai-systems-studio` when the main question is local model choice, deployment path, or hardware-to-stack fit
- `mcp-server-builder` for real tool integration
- `skill-creator` and `skill-reviewer` for reusable workflow packaging
- `skills-search` before building from scratch
- `prompt-optimizer` for prompt quality work
- `deep-research` when the workflow depends on structured external knowledge

## Triggers

Common requests that should trigger this skill:
- "Help me turn this into an agent workflow"
- "How should I structure this workflow now that I know the stack?"
- "Should this be a skill, prompt, script, or MCP server?"
- "Make this AI task reusable"
- "Design an eval loop for this workflow"

## Reference

Read [references/checklist.md](references/checklist.md) when you need a compact workflow design checklist.
