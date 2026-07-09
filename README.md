# amex-platinum-benefits

A [Claude skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) for getting full value out of the American Express Platinum Card.

The Platinum carries ~$3,000+ in annual statement credits against an $895 fee — but they reset monthly, quarterly, semiannually, and annually, and unused amounts are forfeited. This skill gives Claude:

- A complete, dated reference of every current credit and perk (amounts, reset schedules, enrollment requirements, fine-print gotchas)
- A usage-ledger workflow so Claude tracks what you've redeemed
- Proactive expiring-credit warnings whenever the skill triggers
- Statement scanning to reconcile redemptions automatically

## Install

**Claude Desktop / Cowork:** Settings → Capabilities → Skills → add this folder (or install the packaged `.skill` file).

**Claude Code:** copy the `amex-platinum-benefits/` folder into `~/.claude/skills/`.

## Usage

Just ask things like:

- "Did I use my Resy credit this quarter?"
- "Will this Uber Eats order trigger my credit?"
- "What Platinum credits expire this month?"
- "Here's my statement — reconcile my credits"

## Structure

```
amex-platinum-benefits/
├── SKILL.md                        # behavior + tracking workflow
├── references/benefits.md          # full benefits reference (dated)
└── assets/usage-ledger-template.md # yearly ledger template
```

## Keeping it current

Amex changes benefits regularly (e.g., the Saks credit ended July 1, 2026). The reference file carries a "Last verified" date; the skill instructs Claude to re-verify via web search when the data is stale. PRs updating `references/benefits.md` welcome.

## Disclaimer

Not affiliated with American Express. Benefit terms change — always confirm in the Amex app before relying on a credit. This is informational, not financial advice.
