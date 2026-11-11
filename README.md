# MyOS

**A personal layer between what I want to do and the information, projects and tools involved in doing it.**

Work in progress: the code and design documents are not public yet. Updated November 2026.

[The idea](#the-idea) · [MyOS Mail](#myos-mail-the-first-piece) · [Still open](#still-open) · [Get in touch](#get-in-touch)

I'm building MyOS for my own work first. It explores how AI can take on the overhead of keeping my work together while I stay in control. "OS" is a metaphor, not an operating system.

## The idea

<p align="center"><img src="docs/images/myos-problem.png" alt="My work arrives in pieces, and I hold it together: nine pieces from email, calendar, course site, files, chat, notes, a project repo and a cloud drive all reach me; I recover the context, coordinate the pieces and remember all of it myself" width="100%"></p>

**Constraints.** Whatever takes over this work must leave me in control, because AI can be wrong. My information must stay mine: readable, traceable and recoverable.

<p align="center"><img src="docs/images/myos-model.png" alt="What MyOS is: an interface between sources and the user. Sources are read into MyOS; an AI secretary, given authorized context, writes the Interpretation layer; the user views it and decides; only decisions change the Personal state, kept as files" width="100%"></p>

<p align="center"><img src="docs/images/myos-rules.png" alt="Three rules: sources stay put (read, not changed); AI proposes, I decide (capability is not autonomy); my files hold the truth (every view can be rebuilt from them)" width="100%"></p>

**The open question.** Links, dates and project views have helped people keep track of their work since Bush's memex and early hypertext, but keeping them up to date by hand costs attention. MyOS tests whether AI can do this upkeep cheaply enough once my own checking and corrections are counted. This is a hypothesis, not a result.

**Where it stands.** The model and a small set of design principles are written down; the architecture is still open and will follow from use. The first piece built on them is MyOS Mail.

## MyOS Mail, the first piece

Mail is the first source MyOS works on, because most commitments arrive there.

### Design and philosophy

<p align="center"><img src="docs/images/mail-costs.png" alt="Each email costs me five things, all at once: notice, triage, decide, remember and check. In mail today I pay all of them the moment an email arrives; in MyOS Mail the email waits for my review time, AI writes one line on what it means, I decide once in one list, the app keeps it and brings it back, and the source sentence is one tap away" width="100%"></p>

**Constraints.** Attention is scarce, and interruptions cost more than they last. AI can be wrong, so I must see where each claim comes from. Nothing in my plans may change without me.

<p align="center"><img src="docs/images/mail-before-after.png" alt="From messages to matters. Now: twelve emails pile up as twelve alerts and look alike, and an urgent venue change is buried among them. With AttentionMail: new mail waits for the 18:00 review; a change to today comes through at once; the review lists what each email would change for my plans, I confirm once, and Today keeps the plan" width="100%"></p>

<p align="center"><img src="docs/images/mail-design.png" alt="The design, in the AttentionMail phone prototype with made-up emails: at 15:00 Today shows my plans, not my inbox; at 16:39 only a change to today comes through; at 18:06 I decide once in one list; at 18:07 I can check any AI claim against its source; on Thursday a deadline comes back in time" width="100%"></p>

The phone design, AttentionMail, is a clickable prototype with made-up emails. It was usability-tested with students, and testing changed how the review status is worded.

### How it is built (ongoing)

One app runs on my Mac and serves the Mac and my phone from the same state. It implements the model and the three rules above. The code is not public yet; the screenshots use its built-in sample of made-up emails.

<p align="center"><img src="docs/images/mail-app.png" alt="The running app with made-up emails: the evening review on the Mac, an email with the AI line and its highlighted source sentence on the phone, and Today on the phone after the review" width="100%"></p>

Two engineering choices follow from the rules above. It reads Apple Mail's own files instead of asking Mail to open messages, so reading can never change my mail. AI notes are stored apart from my decisions, so a new AI answer can never overwrite what I decided.

## Still open

- How to build the personal file system? It still remains a lot of questions (like agent harness) even we constrained it to markdown files with Obsidian philosophy. 
- How to control the boundaries of AI agent while keep human in control?
- The privacy issue.
  
## Get in touch

If you are working on similar ideas or have thoughts on any of this, please open an issue here or reach me through jsx7701@icloud.com.  I would be glad to hear from you.

---

MIT licensed.
