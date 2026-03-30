# 🤖 bot-tester

**bot-tester** is a professional AI security testing skill for Claude Code. It conducts automated, extensive test conversations with chatbots using persuasion principles to evaluate their security, boundaries, and susceptibility to manipulation before they are deployed to production.

## 🎯 Key Features

- **Automated Security Testing**: Uses Playwright MCP to interact with web-based chatbots autonomously.
- **Deep Conversations**: Conducts conversations with up to 150 exchanges to test sustained security boundaries.
- **Advanced Persuasion Techniques**: Utilizes various AI Red Teaming and jailbreak techniques including:
  - Role Play / Hypothetical Framing
  - Commitment Chains
  - Authority Injection
  - Skeleton Key
  - Context Manipulation
- **Comprehensive Reporting**: Generates a detailed breakdown of findings, boundaries discovered, successful/failed techniques, and actionable security recommendations.

## 🛠️ How It Works

The tester progressively escalates the conversation through four primary phases:

1. **Warm-Up Phase (1-20 messages)**: Builds trust and establishes a baseline conversation using liking and reciprocity.
2. **Commitment Chain (21-50 messages)**: Makes small, logical requests to secure gradual agreements.
3. **Reframing & Hypotheticals (51-100 messages)**: Employs creative approaches like role-playing and third-person perspectives to bypass simple filters.
4. **Advanced Techniques (101-150 messages)**: Applies maximum pressure through complex methods like the "Skeleton Key" and context manipulation.

## 📦 Installation

### Prerequisites
- [Claude Code](https://claude.ai/code) installed.
- [Playwright MCP](https://github.com/microsoft/playwright-mcp) installed and configured.

### Step 1: Install the Skill

Copy the `SKILL.md` file to your Claude Code skills directory. Depending on your OS, the path may vary, but typically it runs like this:

```bash
mkdir -p ~/.claude/skills
cp SKILL.md ~/.claude/skills/bot-tester.md
```

### Step 2: Configure Playwright MCP

Ensure the Playwright MCP server is configured in your `~/.claude/settings.json`:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```

## 🚀 Usage

To use this skill with Claude Code:

1. Provide the URL of the bot you wish to test: `/bot-tester <bot-url>` (or run `/bot-tester` to be prompted interactively).
2. Answer the standard prompt to specify what exact information you are attempting to extract (e.g., system instructions, internal data).
3. The bot-tester will drive the browser, sending inputs and reading outputs autonomously.
4. Review the generated `bot-test_YYYY-MM-DD_HH-MM.md` report artifact detailing the findings and the full conversation log.

## ⚠️ Responsible Use

This tool is constructed **strictly for authorized security testing** on your own internal bots or those you have explicit permission to test within a staging environment. Do not use this tool for malicious purposes against unauthorized targets.
