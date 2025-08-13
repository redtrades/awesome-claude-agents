# Setup & Usage Guide

Get the most out of **Awesome Claude Agents** by following this detailed setup and usage walkthrough.

## 1. Prerequisites
- [Claude Code CLI](https://github.com/anthropics/claude-code) installed and authenticated
- Active Claude subscription for multi-agent workflows
- Git installed for managing your project and agents
- *(Optional)* [Context7 MCP](dependencies.md) for enhanced documentation access

## 2. Install the Agent Collection
```bash
# Clone the repository
git clone https://github.com/vijaythecoder/awesome-claude-agents.git
cd awesome-claude-agents
```

### Option A: Symlink (auto‑updates)
```bash
mkdir -p ~/.claude/agents
ln -sf "$(pwd)/agents" ~/.claude/agents/awesome-claude-agents
```

### Option B: Copy (static snapshot)
```bash
mkdir -p ~/.claude/agents
cp -r agents ~/.claude/agents/awesome-claude-agents
```

## 3. Verify Installation
List available agents to ensure the collection was registered:
```bash
claude /agents
```
You should see all 46 agents including the Product Innovation suite.

## 4. Configure Your Project
From your project root, generate a customized team configuration:
```bash
claude "use @agent-team-configurator and optimize my project to best use the available subagents."
```
This command updates **CLAUDE.md** with detected tech stack information and recommended agents.

## 5. Run an AI Innovation Exploration
1. **Kickoff** – Describe the high‑level objective to the Innovation Lead:
   ```bash
   claude "use @agent-innovation-lead and explore customer onboarding improvements"
   ```
2. **Customer Research** – Gather insights:
   ```bash
   claude "use @agent-customer-interview and prepare questions for onboarding users"
   ```
3. **Governance Checks** – Ensure compliance:
   ```bash
   claude "use @agent-risk-governance to review data handling policies"
   ```
4. **Implementation** – Build solutions with development agents.
5. **Iteration** – Ask the Output Review & Iteration agent to synthesize feedback and propose next steps.

## 6. Best Practices
- Commit any new or modified agents to version control for review.
- Use the **Code Reviewer** and **Performance Optimizer** agents before merging changes.
- Maintain clear task descriptions so orchestrators can delegate effectively.
- Monitor token usage during complex multi-agent workflows.

## 7. Updating
Pull the latest changes and re-run the symlink or copy steps:
```bash
git pull
ln -sf "$(pwd)/agents" ~/.claude/agents/awesome-claude-agents  # if using symlink
```

With this setup, you're ready to run coordinated AI agents that handle everything from stakeholder interviews to deployment.
