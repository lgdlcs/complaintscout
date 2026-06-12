# ComplaintScout — Free Sample Report for Kikubot

**Prepared for:** asp68 (HN) · [Show HN: Kikubot – Each AI agent is an inbox](https://news.ycombinator.com/item?id=48492034)
**Pain point searched:** *"Deploying AI agents in a real company is too complex — frameworks slow you down, non-technical staff won't open another dashboard"*
**Window:** last 90 days · **Sources:** Reddit + Hacker News
**Date:** 2026-06-12 · **This free sample:** 10 leads (a paid report has 25) · permalinks checked live today

> **How to use this.** These are people who publicly complained about, or asked for help with, exactly the problem Kikubot solves: getting agents adopted without a new orchestrator, a new UI, or a new login. Reply where a public answer adds value, DM where it's personal. Lead with their problem, never with your link. Suggested cadence: 3–5 contacts/day.
>
> *Quotes marked (title) are the post's headline verbatim; paid reports include full-body quotes for every lead.*

---

## Lead 1 — FailMore (HN) · ★★★ (posted the same pain TWICE in 4 days)

- **Where:** [HN 48112288](https://news.ycombinator.com/item?id=48112288) (2026-05-12) + [HN 48157211](https://news.ycombinator.com/item?id=48157211) (2026-05-16)
- **Verbatim (title):** "After extensive work with agents, the non-technical sentence is the shape I see"
- **Why hot:** posting the same thesis twice in one week is the strongest signal in this batch. His whole point is that the natural interface to agents is a plain sentence written by a non-technical person — which is literally an email. He has already argued himself into your architecture.
- **DM draft (from asp68):**
  > Your "non-technical sentence" posts kept coming back to me while building Kikubot — I think we converged on the same conclusion from different ends. I made every agent an email address: the non-technical sentence IS the protocol, the inbox IS the UI, and the roster handles routing. OSS, no orchestrator. Would genuinely value your take, since you wrote the thesis before I shipped the implementation.

## Lead 2 — u/Practical_Low29 · ★★★

- **Where:** [r/AI_Agents](https://www.reddit.com/r/AI_Agents/comments/1tps2wh/wheres_the_line_between_agent_framework_helping/) · 2026-05-28
- **Verbatim (title):** "where's the line between agent framework helping vs slowing you down?"
- **Why hot:** asking the exact question Kikubot answers with "no message queue, no vector store, no orchestrator".
- **DM draft:**
  > Your "helping vs slowing you down" question is the one I rage-quit a framework over. My answer ended up being: the framework should disappear into infrastructure you already run. I built Kikubot around email as the message bus — every agent is an address, routing is a roster, and there's no orchestrator to babysit. OSS if you want to poke at it; mostly I'm curious where you ended up drawing the line.

## Lead 3 — u/Worried_Market4466 · ★★★ (already built his own runtime — your exact audience)

- **Where:** [r/AI_Agents](https://www.reddit.com/r/AI_Agents/comments/1tjljur/built_my_own_agent_runtime_after_hitting_the/) · 2026-05-21
- **Verbatim (title):** "Built my own agent runtime after hitting the ceiling with LangGraph — UI as graph nodes, Postgres durability"
- **Why hot:** hit the framework ceiling hard enough to build his own runtime. People like this adopt, contribute to, and evangelize OSS alternatives — a design-partner profile, not just a user.
- **DM draft:**
  > "Hitting the ceiling with LangGraph" — same wall, different exit. You went runtime + Postgres durability; I went email-as-message-bus (every agent is an inbox, SMTP is the queue, the audit log is your mail archive). Two contrarian answers to the same ceiling. Would love to trade war stories — and if you see an obvious hole in the email approach, you're the right person to find it.

## Lead 4 — growt (HN) · ★★

- **Where:** [Manifesto for Agentic Teams](https://news.ycombinator.com/item?id=48476888) · 2026-06-10
- **Verbatim (title):** "Manifesto for Agentic Teams – reorganizing engineering around AI agents"
- **Why hot:** he's writing the org-design layer; Kikubot's coordinator + roster is an implementation of it. Manifesto authors want implementations to point at.
- **DM draft:**
  > Read your agentic-teams manifesto — the org-chart framing is the part most agent frameworks ignore. Kikubot is basically that manifesto as infrastructure: each agent is an email address, a coordinator keeps a roster of capabilities and routes work like a team lead would. If you're collecting real-world implementations for a follow-up, happy to be a case study (it's OSS).

## Lead 5 — u/Upper_Bass_2590 · ★★ (lost $8k to enterprise adoption friction)

- **Where:** [r/AI_Agents](https://www.reddit.com/r/AI_Agents/comments/1u0mm0o/the_8k_healthcare_mvp_that_broke_at/) · 2026-06-08
- **Verbatim (title):** "The $8k Healthcare MVP That Broke at Procurement (HIPAA BAA that killed it)"
- **Why hot:** his MVP died because it added new infrastructure a compliance team had to approve. "Agents over the email system you already have a BAA for" is a different procurement conversation.
- **DM draft:**
  > Your procurement post-mortem hit home. One angle for the next iteration: the reason email survives every compliance regime is that it's already covered — the BAA, the retention policy, the audit trail all exist. I build agents that live ON email (each agent is an inbox, no new message bus to get approved). Not claiming it fixes HIPAA, but "runs on infrastructure you already signed for" changes who you have to convince. Happy to compare notes.

## Lead 6 — u/New_day4 · ★★ (the non-technical buyer)

- **Where:** [r/smallbusiness](https://www.reddit.com/r/smallbusiness/comments/1tunkel/how_are_you_actually_figuring_out_what_can_be/) · 2026-06-02
- **Verbatim (title):** "How are you actually figuring out what can be automated/streamlined in your business? Feeling kinda stuck"
- **Why hot:** the persona Kikubot's README promises to serve — wants automation without learning an orchestrator. "Email a task to kiku@" is the only pitch this persona can adopt same-day.
- **DM draft:**
  > Saw your "feeling kinda stuck" post. A low-tech way to find what's automatable: anything your team already handles by forwarding an email is a candidate. That's the bet behind Kikubot (OSS thing I built — agents that ARE email addresses: you forward the task, the right agent picks it up). Even if you never use it, "what do we forward today?" is a decent audit question for your list.

## Lead 7 — u/Careless_Leg_4905 · ★★

- **Where:** [r/AI_Agents](https://www.reddit.com/r/AI_Agents/comments/1u2934b/setting_up_claude_code_in_a_legacy_software/) · 2026-06-10
- **Verbatim (title):** "Setting up Claude Code in a legacy software application"
- **Why hot:** legacy environment = the place where "no new infrastructure" wins by default. Email is the one bus a legacy shop already runs.
- **DM draft:**
  > Good luck with the legacy integration — that's where most agent setups quietly die. One thing that helped me: not adding infrastructure at all. Kikubot runs agents as email addresses, so the "integration" with a legacy org is the mail server they've had since 2009. OSS, might be a fit or at least an idea to steal for the parts of the company that will never install anything new.

## Lead 8 — u/ConfusionNo8504 · ★

- **Where:** [r/AI_Agents](https://www.reddit.com/r/AI_Agents/comments/1typ3iw/how_do_you_create_real_agents/) · 2026-06-06
- **Verbatim (title):** "How do you create real agents?"
- **Why hot:** beginner question, but "real" is the operative word — he's frustrated with demos that don't survive contact with actual work.
- **DM draft:**
  > Your "real agents" question deserves a non-demo answer: a real agent is one a colleague can give work to without you in the room. That constraint drove everything in Kikubot (OSS): each agent is an email address, so handing it work is just… sending an email. Happy to walk you through how the roster/routing works if you want a concrete codebase to learn from.

## Lead 9 — jb_briant (HN) · ★

- **Where:** [Tell HN](https://news.ycombinator.com/item?id=48035831) · 2026-05-06
- **Verbatim (title):** "I'm struggling formalizing 15 years of experience to my clodex agent"
- **Why hot:** the knowledge-transfer pain is Kikubot's roster problem from the individual side — describing capabilities so work can be routed.
- **DM draft:**
  > Your Tell HN about formalizing 15 years of experience stuck with me — it's the same problem as writing a good agent roster entry: what does this agent actually know how to do? In Kikubot I ended up keeping capability descriptions short and letting the coordinator learn from routing outcomes instead of front-loading everything. Might be a useful pattern for your clodex setup too.

## Lead 10 — ex-aws-dude (HN) · ★

- **Where:** [Ask HN](https://news.ycombinator.com/item?id=47927175) · 2026-04-27
- **Verbatim (title):** "Will fixed applications become a thing of the past with agentic AI?"
- **Why hot:** if applications dissolve, what remains is the conversation layer — and the oldest one is email. He's asking the question your architecture answers.
- **DM draft:**
  > Your Ask HN about fixed applications — my bet is they don't disappear, they collapse into inboxes. I built Kikubot on that thesis: no app UI at all, every agent is an email address and the "application" is whatever conversation you have with it. OSS. Curious whether that matches the future you were sketching or breaks it.

---

## Market note (bonus)

Three Show HN launches in the last 48 hours alone target adjacent slices of this pain — AgentStore (datastore for agent teams), Spanly (MCP observability), Multica (business-agent orchestration). The "agents in companies" space is crowding fast, but every competitor adds a dashboard. Kikubot is the only one in this batch removing one. The leads above are being courted right now — speed matters.

---

*This is a free sample of [ComplaintScout](https://lgdlcs.github.io/complaintscout/) — 25 people who publicly complained about the exact problem your SaaS solves, with a DM draft for each. $19, delivered in 48h, pay only if it's useful.*
