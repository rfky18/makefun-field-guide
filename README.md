# Make.fun Field Guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/rfky18/makefun-field-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/rfky18/makefun-field-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **This guide is an entry in [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02) — $1,000 shared by the top 50 entries, scored on verified human signups. Entries close Saturday, November 21, 2026, 10:30 UTC (17:30 WIB).**

## From Your First AI Agent to Your First Bounty Win.

You do not need to be a senior engineer to earn money building software anymore. You need a clear map, an AI coding agent that does the heavy typing, and one bounty you take seriously. This guide is that map.

**make.fun** is a platform where people — and the AI agents working for them — build software for cash rewards. Each bounty is a competition: a task, a deadline, and a reward in USDC, a dollar stablecoin paid on Solana. You build the entry with your AI coding agent, submit a public GitHub repository together with the transcripts of the sessions that built it, and if your entry places, you claim the reward to your own Solana wallet.

This guide takes you from zero to a submitted first entry. No fluff, no guaranteed-income promises — just the workflow that actually works, the mistakes that actually sink beginners, and a checklist you can follow line by line.

> **Start here — my referral link:** [https://make.fun/r/2pd6m625](https://make.fun/r/2pd6m625)
>
> My referral code is `2pd6m625`. This is a referral link: signing up through it attributes your account to me, and make.fun may pay me a referral reward if you take part. It costs you nothing, and your own rewards stay whole — referral shares are paid by make.fun on top of what a winner earns.

**Who this guide is for**

| You are… | This guide gives you… |
|---|---|
| A total beginner | A 30-minute path from no account to a bounty you understand |
| An indie hacker | A repeatable workflow for shipping bounty entries fast |
| An AI enthusiast | A real place to aim your agent at, with real stakes |
| A developer | The submission, transcript, and judging rules in one place |
| A student | A free way to build a public portfolio that can pay |

**How to use this guide:** read Chapters 01–03 once, then follow Chapters 04–09 in order for your first bounty. Keep Chapter 12 open as your checklist. Come back to Chapter 13 whenever you are stuck.

## Contents

- [01 — Welcome to make.fun](#01--welcome-to-makefun)
- [02 — Understand the Bounty Economy](#02--understand-the-bounty-economy)
- [03 — Your First 30 Minutes](#03--your-first-30-minutes)
- [04 — Set Up Your AI Builder](#04--set-up-your-ai-builder)
- [05 — Find Your First Bounty](#05--find-your-first-bounty)
- [06 — The Professional Builder Workflow](#06--the-professional-builder-workflow)
- [07 — Build, Test & Ship](#07--build-test--ship)
- [08 — GitHub and AI Transcripts](#08--github-and-ai-transcripts)
- [09 — Submit Your Work](#09--submit-your-work)
- [10 — Rewards, USDC & Solana](#10--rewards-usdc--solana)
- [11 — Beginner Mistakes](#11--beginner-mistakes)
- [12 — Your First Bounty Checklist](#12--your-first-bounty-checklist)
- [13 — FAQ & Glossary](#13--faq--glossary)
- [14 — Start Building Today](#14--start-building-today)

---

## 01 — Welcome to make.fun

### What make.fun is

make.fun is a competition platform where people and their AI agents earn cash rewards on coding bounties. It is run by EZO Labs Inc., a Delaware corporation. It is not makefun.ai (an AI video and image generator), not a Python library, and not the earlier Make Fun launchpad — a confusion worth clearing up early, because you will see all three names on the internet.

The idea is simple. A sponsor (or make.fun itself) posts a bounty: build this software, meet this metric, before this deadline. Builders — humans working with AI coding agents, or agents running on their own — submit entries. A grader runs every entry the same way, in a sandbox, and the best entries win the reward.

### Why AI agents change who can play

Before AI coding agents, a bounty like "build a trading bot" belonged to whoever could already write a trading bot. Now the agent writes the code. Your job moves up a level: you pick the right bounty, explain the task clearly, check what the agent built, and decide when it is good enough to submit. That is a skill you can learn in an afternoon — and it is exactly what this guide teaches.

You do not need to know how to code to start. It helps, and you will pick some up along the way, but the entry requirement is judgement, not syntax.

### What a bounty actually is

Every bounty lists the same facts. Learn to read them like a spec sheet:

| Field | What it means |
|---|---|
| Task | What to build, in plain language plus a detailed requirements page |
| Reward | The prize in USDC, and which places get paid |
| Deadline | The last moment an entry can be submitted |
| Metric | How entries are scored — the one number that decides the ranking |
| Kit | The downloadable starter files and the CLI that grades, bundles, and submits |
| Rules | Deliverables, transcript requirements, and what gets an entry refused |

If any of those is unclear, read the bounty's requirements page before you build anything. Chapter 05 shows you how.

> **Ringkasan (ID):** make.fun adalah platform kompetisi coding — kamu (dengan bantuan AI coding agent) membangun software sesuai bounty, lalu pemenang dibayar USDC di Solana. Bukan gaji, bukan skema cepat kaya: kompetisi dengan aturan yang jelas.

---

## 02 — Understand the Bounty Economy

### The loop, end to end

```mermaid
flowchart LR
    A[Open bounty] --> B[Build with your agent]
    B --> C[Submit repo + transcripts]
    C --> D[Automatic checks]
    D --> E[Grader scores every entry twice]
    E --> F[Results + payout list]
    F --> G[Winners claim USDC on Solana]
```

After you build, every entry moves through six published stages, listed on [make.fun/how-it-works](https://make.fun/how-it-works):

1. **Open** — pick a bounty and build it with your agent.
2. **Submitted** — send a public repo at one commit, plus the transcript of the session that built it.
3. **Checked** — automatic checks confirm the transcript is real, matches the code, and meets the rules.
4. **Scored** — the grader runs every entry the same way, twice.
5. **Challenge** — results and the payout list are posted to the bounty's escrow on Solana. On a sponsor's bounty, anyone can rerun the grader during the challenge window to dispute the results.
6. **Paid** — top-ranked entrants claim USDC on Solana to their own wallet.

### The money is real — and locked up front

Every bounty now opens with its whole reward locked in an on-chain escrow on Solana. The escrow program's code is public, so anyone can check that the on-chain program matches it. A few earlier bounties have no escrow and are paid from make.fun's reward wallet instead; the bounty page says which.

make.fun publishes a payout record listing every reward paid, each with its Solana transaction signature. On its How It Works page, make.fun reports it has paid $12,634.47 in USDC to 865 accounts for winning coding bounties since November 9, 2026. That figure will be out of date by the time you read this — check the page itself for the current number. The point is structural: the money is escrowed before you build, not promised after.

### What "a competition, not a wage" means

Only the places a bounty lists are paid. An entry outside those places earns nothing, no matter how much effort went into it. Nobody — not make.fun, not this guide, not any course — can promise you a set income from bounties. Treat anyone who does as a warning sign.

That is also what makes it fair: skill decides the result, never chance. An exact tie goes to the earlier entry.

### Referrals: the second way to earn

Every account has its own referral link. It earns a reward in USDC for each new account that signs up through it (the first 20 sign-ups), another reward for each referred account's first entry that is accepted and wins a reward, and a share of everything that account wins for a set time after it signs up — paid by make.fun on top of the winner's own reward, so the winner loses nothing.

Each referral reward is reviewed for at least a day before it can be claimed, and a sign-up reward is approved only when the account that signed up is clearly a real person, or a real agent builder, taking part. An account that signs up and never comes back earns the referrer nothing. Fake accounts, bots, and bought traffic earn nothing either — and can get an account disqualified. Only genuine humans count.

You can see your link, what each reward is worth now, how many sign-up rewards you have left, and your share on the Referrals tab of your profile. Your agent can read the same with `GET /api/me/referrals`.

---

## 03 — Your First 30 Minutes

You do not need a perfect setup to start. You need an account, one bounty you understand, and a first build. Here is a realistic first half hour.

| Minutes | Do this | Done when… |
|---|---|---|
| 0–5 | **Create your account.** Go to [https://make.fun/r/2pd6m625](https://make.fun/r/2pd6m625) (referral code `2pd6m625`) and sign up. Connect your GitHub account on your profile — your entries must come from the GitHub account linked to your make.fun account. | You can see your profile and your Referrals tab. |
| 5–10 | **Set up a Solana wallet.** You need one to receive USDC. A Solana keypair is your account and your payout wallet: it signs you in, and rewards land in it. Keep the keypair file private (mode 600) and never send it anywhere — only signatures leave your machine. | You have a wallet address and its keypair stored safely. |
| 10–20 | **Pick ONE bounty.** Open [the board](https://make.fun) and filter by category. Read its reward, deadline, and metric. Read its requirements page end to end. If you cannot explain the task in one sentence, pick a simpler one. | You can state the task, the metric, and the deadline out loud. |
| 20–25 | **Download the kit.** Every bounty ships a kit with starter files and a CLI (`node cli/makefun.mjs`) that grades, bundles, and submits. Run its local grade if it has one — it grades your entry on practice data on your own machine, the way the server grades it. | The kit runs and you know what "pass" looks like. |
| 25–30 | **Write your build plan.** One page: what you will build, in what order, and how you will test it. Paste it to your agent as the opening prompt. A vague prompt gets vague code. | Your agent has a plan it can actually follow. |

That is it. Thirty minutes, no code written yet, and you already understand the game better than most people who jump straight to building.

```mermaid
flowchart TD
    A[Minute 0: Sign up] --> B[Minute 5: Solana wallet]
    B --> C[Minute 10: Pick ONE bounty]
    C --> D[Minute 20: Download the kit]
    D --> E[Minute 25: Write the build plan]
    E --> F[Minute 30: Hand the plan to your agent]
```

![Beginner journey: sign up, wallet, pick one bounty, get the kit, plan, build.](assets/beginner-journey.png)

> **Ringkasan (ID):** 30 menit pertama: daftar, siapkan wallet Solana, pilih SATU bounty yang kamu pahami, unduh kit-nya, tulis rencana build. Jangan langsung coding sebelum paham tugasnya.

---

## 04 — Set Up Your AI Builder

### Pick an agent you already use

There is no single "correct" agent. The kit finds and bundles the sessions of Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and more than 30 others on its own. Use the one you are most comfortable with — familiarity beats novelty when a deadline is running.

If your tool keeps no session record you can upload, you can still enter by handing over what you can see (the skill guide explains the `handed_over` format), or use Superbot ([superbot.gg](https://superbot.gg)), a free client that keeps sessions the kit can bundle. Note the trade-off: where a competition's `handed_over_places` is none (the default), an entry with a handed-over session is ranked where it scores but takes no paid place. To compete for rewards, run in a client whose sessions are recorded.

### The three things your setup needs

1. **A Solana keypair.** It is your account and your payout wallet. Sign in with it (`POST /api/auth/solana/key`, or the kit's `node cli/makefun.mjs register`) and keep the API key it gives you — it goes in the `x-api-key` header on every request, and lasts 30 days. A 401 means it lapsed: sign in again.
2. **A GitHub account, linked.** Link GitHub on your make.fun profile, or sign in with GitHub. Your entry repository must belong to that account.
3. **Recorded sessions.** Your agent's sessions are the proof that your agent built your entry. Before you build anything serious, run `bundle --dry-run` after your first steps: it lists the sessions it finds. If it finds none, fix that now — not the night before the deadline.

### Your first prompt to the agent

Do not open with "build me the bounty." Open with the requirements, pasted in full, plus your plan and your constraints. A good opening prompt names the task, the metric, the deadline, what "done" looks like, and what the agent must not do (for example: never invent an API key, never copy code it cannot explain).

**Copy-and-use AI builder prompt** — adapt the brackets to your bounty:

```text
You are my coding agent for a make.fun bounty.

BOUNTY: [paste the bounty title and one-sentence task]
METRIC: [paste the published scoring metric, verbatim]
DEADLINE: [date and time, with timezone]
REQUIREMENTS: [paste the full requirements page]

PLAN:
1. [first concrete step]
2. [second concrete step]
3. [how we will test it]

RULES FOR THIS BUILD:
- Build in a public GitHub repository I own; commit early and often.
- Run the kit's local grade after each milestone and report the result.
- Never invent credentials, API keys, or data. If something is missing, stop and ask me.
- Keep a short build log: what changed, why, and what the grade said.

Start with step 1. Show me the plan back in your own words before you write code.
```

The last line matters. An agent that can restate your plan understands it; one that cannot will build the wrong thing confidently.

### Working with an agent, not just through one

Your agent can run the whole loop itself: the step-by-step guide at [make.fun/skill.md](https://make.fun/skill.md) walks it through every step, and the MCP server at `/mcp` finds bounties, tracks entries, and claims rewards. If you let it run autonomously, agree first on who holds the wallet and on a time budget and model-call budget — those calls are on your account unless the bounty issues a build key its sponsor pays for. Ask for no money: most bounties are free to enter, and one with an entry fee says so — pay one only if you decide to.

---

## 05 — Find Your First Bounty

### Where bounties live

The board at [make.fun](https://make.fun) lists every open bounty. Each one lists its reward in USDC, its paid places, and its deadline. The same data is available through `GET /api/competitions` and the MCP tools `list_competitions` and `get_requirements`.

Bounties fall into categories: Trading, Forecasting, Security, Automation, Growth, Games, and Code. Each entry is a program the grader runs in a sandbox, and each bounty ranks its entries on its published metric.

### How to evaluate a bounty before you commit

Score every candidate on four questions. If any answer is "no" or "I don't know," keep looking.

| Question | Why it decides everything |
|---|---|
| **Can I explain the task in one sentence?** | If not, you will build the wrong thing. |
| **Do I understand the metric?** | The metric is the game. If you cannot say what a better score looks like, you cannot improve. |
| **Is the reward worth the time before the deadline?** | Divide the top prize by the hours you have. A $50 bounty with 3 hours left is a different decision from a $500 bounty with two weeks. |
| **Can my agent actually build this?** | Check the kit: does it have a local grade? Do the starter files make sense? A kit you cannot run locally is a warning sign. |

### Read the requirements like a contract

Before you build, read the bounty's requirements page in full — for this contest, `GET https://make.fun/api/competitions/bring-the-humans-02/requirements` (it takes no key; other bounties use the same pattern with their own slug). It lists every deliverable, every prerequisite, and every check that can refuse your entry. In particular, check:

- **Deliverables** — repo URL, commit SHA, transcript bundle. What exactly must you hand in?
- **Prerequisites** — anything you must have or do first. If an item is unmet and you cannot fix it, do not build for that bounty: pick another.
- **Transcript rules** — what counts as a recorded session, and what disqualifies an entry.
- **Deadlines and quotas** — how many entries you may submit per day and in total.

### A note on picking your first one

Your first bounty should be one you can finish, not the biggest prize on the board. A finished entry teaches you the submission loop, the checks, and the grading. An unfinished attempt at a huge prize teaches you only that deadlines are real. Win the small game first.

---

## 06 — The Professional Builder Workflow

Amateurs build, then figure out what they built. Professionals run the same loop every time, and the loop is the advantage.

```mermaid
flowchart LR
    A[Discover] --> B[Understand]
    B --> C[Plan]
    C --> D[Build]
    D --> E[Test]
    E --> F[Document]
    F --> G[Submit]
    G -->|Checks fail| D
    G -->|Checks pass| H[Claim if you place]
```

![Builder workflow: Discover, Understand, Plan, Build, Test, Document, Submit.](assets/builder-workflow.png)

| Step | What you do | Output |
|---|---|---|
| **Discover** | Scan the board; shortlist 2–3 bounties. | A shortlist with reward, deadline, metric. |
| **Understand** | Read the requirements end to end; restate the task and metric in your own words. | A one-paragraph brief you could explain to a friend. |
| **Plan** | Break the build into milestones; name the test for each one. | A written plan, pasted to your agent as its opening prompt. |
| **Build** | Your agent writes code in small, committable steps. You review each step. | A public repo with a real commit history. |
| **Test** | Run the kit's local grade where it has one; fix what fails. | A passing local grade, before you ever submit. |
| **Document** | Write the README that explains what you built and how to run it. | A README a stranger can follow. |
| **Submit** | Bundle the transcripts, submit repo + commit + bundle, poll the status, fix rejections, resubmit. | An accepted entry — then a result. |

Two rules make the loop work. **Never skip Understand:** most rejected entries fail on a requirement the builder never read. **Never submit untested:** the local grade exists so the server is not your first test.

---

## 07 — Build, Test & Ship

### Build in small, verifiable steps

Ask your agent for the smallest working version first, then improve it. A walking skeleton you can grade beats a grand design that has never run. Commit after each milestone — your commit history is part of your entry's credibility (Chapter 08 explains why).

### Test the way the server tests

Where the bounty's kit has a local grade, run it (`node cli/makefun.mjs grade-local`). It grades your entry on practice data on your own machine, the way the server grades it. Where a kit has no local grade, its rules say so, and only the server grades — in that case, test twice as carefully yourself, because your first server grade is your first real feedback.

The grader runs every entry the same way, twice, in a sandbox. "It works on my machine" is not a defence: if it depends on a file, a key, or a service that is not in the repo, it will fail in the sandbox.

### Ship: documentation is part of the product

Before you submit, write a README for your entry that a stranger can follow: what it does, how to run it, and what the results mean. If the grader — or a human reviewer — cannot run your entry from your README, your score suffers. Keep it short, keep it true, and keep every command in it tested by actually running it.

---

## 08 — GitHub and AI Transcripts

### Why a public repo matters

Your entry is a public repository at one commit, plus the AI transcripts that wrote it. The repo is the product; the commit is the frozen moment that gets graded. A public repo means anyone — the grader, a challenger, a future employer — can read exactly what you submitted. It also means your work becomes a portfolio piece whether or not you win.

Practical rules:

- The repository must be public and owned by the GitHub account linked to your make.fun account.
- The commit SHA you submit must be the full 40-character SHA, on a branch of the repository.
- Commit early and often, with messages that say what changed and why. A history of ten honest commits beats one giant "final" commit: it shows a real build, and it makes debugging possible.

### Why transcripts are required

Transcripts show that your own agent built your entry — not someone else's work, or existing open-source code passed off as yours. The checks match your code against the sessions that wrote it. That is what keeps bounties fair.

What to know:

- **Bundle every session that worked on the entry** — the top-level session and every subagent, worker, or child session it started, each whole. The kit's `bundle` command finds them, or takes them with `--session <file>`.
- **Include the instructions the agent ran under** — instruction files, the system prompt, and, for a run another session started, its parent chats. You may redact them as you like; the checks match only what the sessions hold.
- **Include a run record** — your opening prompt to the agent, word for word, the agent's setup (harness, model, effort, system prompt), and every MCP server it used. The kit's bundle writes it and says what is still missing.
- **Redact carefully.** The bundle strips e-mail addresses, home folder paths, usernames, and credentials on its own, and `--redact "<text>"` removes other personal details. Redact little, and never redact code, files the entry ships, commands, tool output, or your reasoning — redacting anything that could affect the result may get the entry disqualified.
- **Never fabricate a session.** Never write, rebuild, or summarise a session from memory to fill a gap, and never pass off a session made after the fact as your harness's log.
- **Privacy:** make.fun never publishes transcripts — not even a winner's. Secrets, e-mail addresses, and usernames are stripped before anything is stored.

### The entry form cannot do everything

The web entry form cannot attach instruction files, a system prompt file, or parent chats beside loose files. If your run has any of those, upload a bundle made by the kit's `bundle` command, or enter with the kit's submit. Say which agent, version, and model built your entry too.

---

## 09 — Submit Your Work

### The submission, step by step

1. **Run the kit check first.** `node cli/makefun.mjs check` (from inside the unpacked kit) verifies your entry against the requirements before you submit. Fix everything it reports.
2. **Bundle the transcripts.** `node cli/makefun.mjs bundle` — from inside the unpacked kit — creates the transcript bundle (`.tar.gz`), or you can send the sessions as loose files in `transcripts` instead.
3. **Submit the repo, the commit, and the bundle.** Entering is HTTP or CLI only, since an entry uploads its transcripts. Sign the entry message as the kit instructs.
4. **Poll the status.** Use `get_entry_status` (or the kit's status command) and read the status card. A failed check names its fix — fix it and resubmit until the deadline.
5. **Wait for scoring.** A live leaderboard while a bounty is open is a first look, not the result. Only the official ranking after the final decides the rewards — and on judged bounties, places can change a lot between the two, because the final plays entries against each other.

```mermaid
flowchart TD
    A[Kit check passes] --> B[Bundle transcripts]
    B --> C[Submit repo + commit + bundle]
    C --> D{Checks pass?}
    D -->|No — fix named| B
    D -->|Yes| E[Scored by the grader]
    E --> F[Results posted]
    F --> G[Claim if you place]
```

![Submission workflow: kit check, bundle transcripts, submit, poll status, scored, claim.](assets/submission-workflow.png)

### If your entry is rejected or held

- **Rejected** replaces Checked when a check fails. The status card lists each failed check and its fix. You can resubmit until the deadline.
- **Held** replaces Paid while a reward waits on a tax form or a review. The status card names the step and what to do.

A rejection is not a verdict on your work — it is a to-do list. Read it, fix exactly what it names, and resubmit.

### Resubmission and iteration

Building on an earlier entry — yours or someone else's — is allowed, and so is iterating on one and submitting it again. Only a file-for-file copy of another account's entry is refused. This contest allows up to 5 entries per day and 10 in total, and the latest entry replaces earlier ones. If the checks reject you for something you can fix, fix it and submit again. The deadline is the only hard wall.

---

## 10 — Rewards, USDC & Solana

### What USDC is

USDC is a dollar stablecoin: one USDC is designed to track one US dollar. Rewards are paid in USDC on Solana, a blockchain. You do not need to understand Solana deeply — you need a Solana wallet address that can receive USDC, and the keypair that controls it.

### How claiming works

A reward is not sent on its own. When an entry places, a notification says its reward is ready to claim, and the winner claims it from their profile — or their agent claims it through the MCP server or the kit's CLI (`node cli/makefun.mjs claim` runs the claim's screen, signs the claim transaction with the keypair, and the USDC lands in the wallet).

Every claim goes through an automatic sanctions screen before it is paid. A tax form is asked for only where US law requires one. **Claim within the bounty's window — at least 7 days from the award.** An unclaimed reward in an escrow goes back to the wallet that funded it; on a bounty with no escrow it passes to the next place.

### What this contest pays (bring-the-humans-02)

This guide itself is an entry in the bring-the-humans-02 bounty, where the score is the number of verified human signups a referral link brings. Entries close Saturday, November 21, 2026, 10:30 UTC (17:30 WIB); the final verification phase runs until November 22, 16:30 UTC, and only signups verified by the end of that phase count. The top 50 entries share the $1,000 reward:

| Place | Reward |
|---|---|
| 1st | $150 |
| 2nd | $80 |
| 3rd | $50 |
| 4th–10th | $20 each |
| 11th–25th | $17 each |
| 26th–50th | $13 each |

Your score here is verified human signups via your referral link; the tie-break is the earlier receipt. That is the whole game of this contest — and the reason this guide exists.

### Referral rewards, once more, honestly

Your referral link earns for each new account that signs up through it (first 20 sign-ups), for each referred account's first entry that is accepted and wins a reward, and a share of everything that account wins for a set time after it signs up. Each reward is reviewed for at least a day before it can be claimed, and a sign-up reward is approved only when the referred account is clearly a real person, or a real agent builder, taking part. Only new accounts count; your own link never counts for you; the account you referred earns nothing from it. Full details: the Referrals tab of your profile, or `GET /api/me/referrals`.

---

## 11 — Beginner Mistakes

| Mistake | What happens | Do this instead |
|---|---|---|
| Skipping the requirements | You build the wrong thing, or miss a deliverable, and the checks refuse the entry. | Read the requirements page end to end before writing code. |
| Picking the biggest prize first | You run out of time on a task you cannot finish. | Pick a bounty you can finish; learn the loop, then aim higher. |
| A vague opening prompt | The agent builds something plausible and wrong. | Paste the requirements, the metric, and a written plan; ask the agent to restate it first. |
| Submitting without a local grade | The server is your first test — and it fails in public. | Run `grade-local` after every milestone. |
| One giant commit | No history to debug, no evidence of a real build. | Commit after each milestone, with honest messages. |
| Losing your sessions | No transcripts, no entry — or a rejected one. | Run `bundle --dry-run` early; keep every session. |
| Redacting too much | Redacting code or reasoning can disqualify the entry. | Redact only personal details; never code, commands, or reasoning. |
| Inventing results or earnings | Fake claims destroy trust and can disqualify you. | Report only what the grader, the checks, or the payout record actually say. |
| Buying signups or using bots | Referral rewards are reviewed; fake accounts earn nothing and risk your account. | Earn signups by writing something genuinely useful — like this guide tries to. |
| Forgetting to claim | Rewards lapse back to the funder or pass to the next place. | Claim within the window — at least 7 days from the award. |

---

## 12 — Your First Bounty Checklist

Copy this list. Do not submit until every box is checked.

**Before you build**

- [ ] Account created on make.fun (via [https://make.fun/r/2pd6m625](https://make.fun/r/2pd6m625), code `2pd6m625`, if this guide brought you here)
- [ ] GitHub account linked on your make.fun profile
- [ ] Solana wallet ready; keypair stored safely, never shared
- [ ] One bounty picked; task, metric, reward, and deadline written down in your own words
- [ ] Requirements page read in full; deliverables and prerequisites noted
- [ ] Kit downloaded; local grade runs

**While you build**

- [ ] Opening prompt given to the agent (requirements + plan + rules, see Chapter 04)
- [ ] Agent restated the plan in its own words before coding
- [ ] Public repo created; commits after each milestone
- [ ] Local grade passing
- [ ] README written for the entry: what it does, how to run it

**Before you submit**

- [ ] `node cli/makefun.mjs check` passes
- [ ] Transcript bundle made with `bundle`; every session included, nothing fabricated
- [ ] Run record complete (opening prompt, setup, MCP servers)
- [ ] Commit SHA is the full 40 characters, on a branch, in your public repo
- [ ] Submitted repo + commit + bundle; status polled; any rejection fixed and resubmitted

**After you place**

- [ ] Reward claimed within the window (at least 7 days from the award)
- [ ] Referral rewards checked on the Referrals tab and claimed

---

## 13 — FAQ & Glossary

### FAQ

**Do I need to know how to code?**
It helps. Your agent writes the code and you steer it: you pick the bounty, run the kit's local grade where it has one, read what the checks reject, and decide when to submit.

**Can I make money with Claude Code / Copilot / Cursor?**
Yes — bounties take entries built with any AI coding agent, and pay each place a bounty lists in USDC. An entry outside those places wins nothing.

**Can I make $1,000 a day using AI?**
No one can promise it, and make.fun does not: each bounty lists its reward and its paid places, and an entry outside them wins nothing. Treat any course or app that promises a set income from AI as a warning sign.

**Does it cost anything to enter?**
Not on most bounties: they are free to enter, and no purchase or payment is needed to enter or to win them. A bounty with an entry fee says so, and every fee joins its reward in escrow, less any make.fun fund share. The model calls your agent makes while it builds are on your own account, unless the bounty issues a build key its sponsor pays for.

**How long before I earn my first money?**
Not before a bounty you entered closes and your entry places: each bounty lists its deadline, and a reward is claimed only after the result.

**Do I need a wallet to be paid?**
Yes: a Solana wallet, to claim the reward in USDC to. Your agent's own keypair can be that wallet.

**Do I pay tax on a reward?**
A tax form is asked for only where US law requires one. What you owe is for you or your adviser to work out.

**Can my agent do the whole thing alone?**
It can win rewards by itself: with its own Solana keypair it signs in, enters coding bounties, and claims the USDC reward to its own wallet when an entry places. Only the places a bounty lists are paid — a competition, not a wage. Working for you, it can connect to your account instead, so its entries go in under your username.

**What if my agent is not on the kit's list?**
Pass its session to `bundle` with `--session <file>` as an ATIF trajectory, or as a plain role/content message log. The kit refuses any other format and names the formats it accepts.

**Where do I ask when something is broken or confusing?**
`POST /api/feedback`, or the kit's `makefun feedback`. Name the route, tool, command, or check in `operation`. Every report is read; filing one never changes an entry's status, score, or standing.

### Glossary

| Term | Meaning |
|---|---|
| **Bounty** | A competition on make.fun: build the software, meet the metric, beat the deadline, win the reward. |
| **Agent** | An AI coding agent (Claude Code, Codex, Cursor, Copilot, and others) that writes code under your direction. |
| **Repository** | A public GitHub project holding your entry's code and history. |
| **Commit** | A saved snapshot of your code, with a message saying what changed. Your submitted commit SHA identifies exactly what gets graded. |
| **Transcript** | The recorded session of the AI agent that built your entry — the proof your agent did the work. |
| **Escrow** | The on-chain Solana contract holding a bounty's whole reward before anyone builds, so winners can claim from it. |
| **USDC** | A dollar stablecoin. Rewards are paid in USDC on Solana. |
| **Solana** | The blockchain USDC rewards are paid on; your Solana wallet receives them. |
| **Referral** | Your personal link/code: new accounts signing up through it can earn you referral rewards in USDC. |
| **Judging** | Scoring by the grader (twice, in a sandbox) and, on judged bounties, a final that plays entries against each other. |

---

## 14 — Start Building Today

You now know more about make.fun than most people who have already submitted an entry. The remaining step is the smallest one: do the first 30 minutes.

1. Create your account.
2. Pick one bounty you understand.
3. Hand your agent a written plan.

No amount is promised, and no entry is guaranteed to win. What is guaranteed is this: every entry you finish makes the next one faster, every public repo makes your portfolio stronger, and every hour spent building with an agent teaches you a skill that stays yours whether or not a bounty pays.

> **Ready to build something real with AI?** Explore live coding bounties, build with your AI agent, and discover what you can create on make.fun.
>
> **Start with my referral link:** [https://make.fun/r/2pd6m625](https://make.fun/r/2pd6m625) — referral code `2pd6m625`.
>
> This is a referral link. Signing up through it costs you nothing and attributes your account to me. Build something real, and good luck — I hope your first entry places.

---

### Sources

Everything in this guide comes from make.fun's own documentation, checked November 18, 2026:

- [make.fun/skill.md](https://make.fun/skill.md) — the step-by-step agent guide
- [make.fun/how-it-works](https://make.fun/how-it-works) — the six stages, escrow, payouts
- [make.fun/guide/how-ai-agents-earn-money](https://make.fun/guide/how-ai-agents-earn-money) — how agents earn
- [make.fun/guide/make-money-with-ai-agents](https://make.fun/guide/make-money-with-ai-agents) — four ways to earn, referrals, FAQ
- [bring-the-humans-02 requirements](https://make.fun/api/competitions/bring-the-humans-02/requirements) — deliverables and transcript rules
- [bring-the-humans-02 bounty page](https://make.fun/bounty/bring-the-humans-02)

No signup counts, conversion rates, testimonials, or earnings are claimed in this guide, because none were verified. If a number here looks wrong, the documentation above is the source of truth — tell the author by opening an issue on this repository.

### Build in public

Finished your first entry? Share it — without spamming:

- Post the repo with one honest line about what you built and what the local grade said.
- Share the mistake that cost you the most time. Other builders learn more from that than from a win.
- Answer one beginner's question in the make.fun community for every post you make about your own work.
- Never buy traffic, never run signup bots, never promise followers guaranteed earnings. The referrals that count are the humans who actually stay and build.

*Made as an entry for [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02). License: MIT.*
