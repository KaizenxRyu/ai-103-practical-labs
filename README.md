# AI-103 Practical Labs

Learning AI engineering through a small support assistant: explain, build, test, teach back.

**Author:** Rahul Chamoli / Kaizen-Ryu. **Teacher:** Codex in the learning session.

This is an independent study repository, not an official Microsoft course. The first lesson is ready; no Azure application has been deployed and no lab has been completed by the learner yet.

## How we learn

```mermaid
flowchart LR
    A[Understand the concept] --> B[Choose a design]
    B --> C[Build a small lab]
    C --> D[Test normal and failure cases]
    D --> E[Explain the result in your own words]
    E --> F[Record evidence and lessons]
    F --> G[Draft a LinkedIn explanation for review]
```

Each lesson has a scenario, acceptance criteria, a short practical task and a teach-back question. A teacher demonstration is recorded separately from work the learner completes.

## One project, several lessons

We will build a support assistant using invented product documents. It should cite its sources, say when evidence is missing, and obtain permission before changing a ticket.

```mermaid
flowchart LR
    U[User question] --> A[Assistant]
    D[Synthetic product documents] --> R[Retrieval]
    R --> A
    A --> T[Read-only ticket lookup]
    A --> V[Answer with citations]
    A --> P[Approval for ticket changes]
    P --> W[Bounded write tool]
```

This is the target architecture, not a claim of running integration.

| Lesson | Practical outcome | Initial status |
| --- | --- | --- |
| 01 Design choices | Explain model, retrieval, tools, identity and budget decisions | Ready to start |
| 02 First Foundry call | Make and inspect a Python model request | Planned |
| 03 Grounded answers | Retrieve synthetic notes, cite evidence and handle missing answers | Planned |
| 04 Tools and agent behavior | Inspect tool calls and test a rejected write request | Planned |
| 05 Multimodal workflows | Exercise image, text, speech and document scenarios | Planned |
| 06 Evaluation and revision | Measure failures, review service choices and repeat weak topics | Planned |

The lessons map to the [current AI-103 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-103). They do not replace full syllabus coverage or the official practice assessment.

## This week's focus

| Day | Proposed study focus |
| --- | --- |
| Tuesday 13 October | Diagnostic, design decisions and Foundry setup |
| Wednesday 14 October | Python, retrieval and agents |
| Thursday 15 October | Failure cases, security and multimodal tasks |
| Friday 16 October | Practice, wrong-answer review and rest; exam at 21:45 IST |

## Start here: lesson 01

You are designing an assistant for an invented product, Alpine Desk. Its support procedures change weekly, its ticket status changes throughout the day, and ticket closure needs operator approval.

Answer these three questions in your own words:

1. For changing procedures, would you choose retrieval, a prompt or fine-tuning? Give a reason and a limitation.
2. For the live status of ticket ALP-104, which component supplies the answer? What happens if it times out?
3. Before closing that ticket, what identity, authorization, confirmation and duplicate-request checks should the application perform?

Acceptance: distinguish model behavior, current knowledge and external actions; justify the design; explain a failure path. A generated tool request is not permission to act. These are original teaching questions, not recalled exam questions.

The fuller lesson and learner log are in the local workspace. They will be published alongside reviewed lab implementations.

## Repository layout

```text
docs/
  intent.md          scope and learning boundaries
  status.md          current evidence and next action
  progress.md        learner-completed work and open gaps
  lessons/           scenarios and acceptance criteria
  diagrams/          reviewed architecture diagrams
src/                 Python application modules, added with the labs
tests/               meaningful checks, added with implementation
infra/               bounded Azure definitions, added after setup approval
content/             LinkedIn drafts based on verified work
```

Only existing maintained files are committed; the tree also shows planned code directories. Credentials, raw screenshots, private exam records and deployment state stay out of Git.

## Turning learning into content

One completed lab can produce a short post: problem, illustrated flow, observed result, limitation and repository link. Do not claim production use, a certification pass, client results or learner completion without evidence. Posts require Rahul's review and a separate publish instruction.

## Sources

Checked 13 October 2026:

- [AI-103 blueprint](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-103)
- [Credential and official practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-apps-and-agents-developer-associate/)
- [Foundry retrieval grounding](https://learn.microsoft.com/en-us/azure/foundry/concepts/retrieval-augmented-generation)
- [Foundry agents overview](https://learn.microsoft.com/en-us/azure/foundry/agents/overview)

Use original scenarios and public synthetic data. No exam dumps or copied assessment questions.
