# PITCH KIT - Workflowry n8n v3 Migration Scanner + Auto-Fix

Your tool: https://mehmoodbhutta.github.io/business/scan.html
Landing: https://mehmoodbhutta.github.io/business/

---

## THE CORE PITCH (say this everywhere, 2 sentences)

"n8n 3.0 lands in December and there's no going back - legacy Function, Cron, Interval and old OpenAI/AI-Agent nodes just stop working. I scanned what breaks, built a free tool that checks your workflows AND hands you a fixed file - paste your JSON, download it v3-ready."

---

## THE HOOK NUMBERS (why anyone cares)

- 2,284 of 13,429 public templates (17%) break on upgrade - verified by a community scan
- 1,493 of those die from AI Agent v1 alone
- No downgrade path. v1 support ends Dec 31, 2026.
- Beta is out NOW (Oct 27). Panic window: Nov-Dec.

---

## POST 1 - n8n Forum, "Built with n8n" category (category id 15)

This is the highest-trust channel. Frame it as a contribution, not an ad.

TITLE: I built a free v3-migration checker + auto-fixer: paste your workflow JSON, get a fixed file

BODY:

Hey all - with 3.0 around the corner I kept seeing the same question: "how do I know if my workflows break?"

So I built a tool that answers it. 100% client-side, nothing is uploaded:

**What it does**
1. Paste your workflow JSON (n8n → workflow menu → Download)
2. It checks for: legacy nodes removed in v3 (Function, Cron, Interval, Item Lists, legacy OpenAI, AI Agent v1), unauthenticated webhooks, plaintext credentials, missing error handling, dangling connections, duplicate IDs, node-reference typos, unbalanced expressions, invalid JSON bodies, orphaned nodes
3. One click → it generates a FIXED workflow JSON: legacy nodes swapped for v3 equivalents, retries added, error handling set, missing Respond-to-Webhook nodes created and wired, type mismatches corrected
4. You download the fixed file, import, and review the short "needs your attention" list (things only you can fill in, like your real credentials)

**What it does NOT do**
- It can't verify credentials against your instance or invent secret values
- It won't touch node intent (disabled/orphaned nodes are flagged, not changed)
- Deep logic bugs need a human (that's what I do for a living)

**Honest limits:** it's a static analyzer, not an execution engine. For most workflow structures it catches what would break on upgrade or in production - and the auto-fix handles the mechanical 80%.

Feedback welcome - especially "it missed X" or "it false-alarmed on Y", both make it better.

Link: https://mehmoodbhutta.github.io/business/scan.html

---

## POST 2 - Reddit r/n8n

TITLE: I scanned what breaks in n8n 3.0 and built a free fixer - paste your workflow JSON, download it v3-ready

BODY:

The 3.0 beta is out, stable lands in December, and there's no downgrade path. A community scan of all 13,429 public templates found 2,284 (17%) contain at least one node that v3 removes - 1,493 from AI Agent v1 alone. Your private workflows are probably in similar shape if they're older.

Instead of manually checking every workflow against the breaking-changes doc, I built a tool:

- Paste workflow JSON (nothing leaves your browser)
- It flags everything v3 kills + the usual production killers (open webhooks, plaintext creds, missing retries, silent failures)
- Generates a fixed file: legacy nodes → v3 equivalents, error handling added, missing Respond-to-Webhook created and wired
- Download, import, fill in the flagged credentials, done

It also catches non-migration bugs: node-reference typos (it caught "Send Repy" vs "Send Reply"), unbalanced expressions, invalid JSON bodies, duplicate node IDs, orphaned nodes.

Free, no signup: https://mehmoodbhutta.github.io/business/scan.html

Known limits: static analysis (doesn't execute), won't invent credential values, deep logic bugs are on you. If it misses something or false-alarms, tell me and I'll fix the checker.

---

## POST 3 - Reply template for people asking "will my workflows break in 3.0?"

"Run it through this - paste the JSON, it lists exactly which nodes v3 removes and generates the fixed file: [link]. Runs in your browser, nothing uploaded. If something's still off after the auto-fix, that's the part worth paying a human for."

---

## WHERE TO POST, IN ORDER

1. **n8n forum → Built with n8n** (Post 1) - highest trust, permanent visibility, mods tolerate tools here
2. **r/n8n** (Post 2) - big audience, link-friendly, the "13,429 templates" number carries it
3. **Reply to the 3.0 announcement thread + migration-prep threads** with Post 3 template - warm audience, already panicking
4. **The 48 prospect threads** in outreach/prospects.json - anyone with a broken workflow gets Post 3 + the scanner link
5. Later: HN "Show HN" if the Reddit post gets traction (title: "Show HN: I auto-fix n8n workflows for the 3.0 migration")

## TIMING

Beta dropped Oct 27. Post 1 + 2 TODAY - the panic compounds toward December. Re-post/mention in early November ("stable is X weeks away") and early December ("last chance before the deadline").

## RULES

- Never post the same wording twice on the forum (spam filters) - vary one sentence
- Reply to every comment within 2h for the first 48h - that's what keeps the thread alive
- Every "it missed something" comment = a fix within 24h + a public "fixed" reply - that's your credibility engine
