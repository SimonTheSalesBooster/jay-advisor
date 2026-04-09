# Jay Advisor

Jay is a Claude Code skill that runs 8 Jay Abraham revenue growth frameworks against your business data daily. It identifies the single highest-ROI move you should make this week.

## Setup

1. Copy `jay-advisor.md` to `~/.claude/commands/jay-advisor.md`
2. Copy `.env.example` to `~/.claude/.env` and fill in your keys
3. Run `/jay-advisor` from Claude Code

## Required Environment Variables

- `NOTION_API_KEY` .. your Notion integration token (for CRM + pipeline data)
- `DISCORD_WEBHOOK_AGENTS` .. Discord webhook URL for advisor output
- `DISCORD_WEBHOOK_PIPELINE` .. Discord webhook URL for pipeline alerts

## Optional Environment Variables

- `HUNTER_API_KEY` .. Hunter.io API key for outreach campaign tracking
- `BEEHIIV_API_KEY` .. beehiiv API key for newsletter analytics
- `OBSIDIAN_VAULT_PATH` .. path to your Obsidian vault for task queue and reports
- `GMAIL_CONFIGURED` .. set to `true` if Gmail MCP is connected

## What It Does

Each run:
1. Reads your board cascade (if running with other advisors) or starts fresh
2. Pulls partnership data from Notion
3. Checks outreach campaign performance (Hunter.io + beehiiv)
4. Applies all 8 Jay Abraham frameworks to your current situation
5. Identifies THE ONE THING .. highest-ROI action for this week
6. Runs cross-industry translation .. finds how Duolingo, Costco, or Peloton solved your exact problem
7. Delegates execution tasks to strategy agents (if configured)
8. Posts summary to Discord

## Notion Setup

Jay reads from these Notion databases (set IDs in the skill file):
- Partners DB .. track JV partners, collaboration status, next actions
- CRM Prospecting .. lead pipeline
- Deals .. active deal tracking
- Members .. community membership status

## Customization

Edit the frameworks, voice, and delegation patterns in `jay-advisor.md` to match your business context.
