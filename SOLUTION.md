# Prompt engineering home assessment Solutions

For each of the tasks below, you need to write a prompt that accomplishes the task. As a result, you
need to provide the prompt and the implications of its use.

## Task 1

### Task 1 description

Generate a paragraph in English about Linus Torvalds contributions to software
development and technology innovation.

### Task 1 Solution

**Suggested prompt**

```
You are a careful technical writer who is interested in software development history.
Your task is: Produce a factual English paragraph on the given theme.
Theme: Linus Torvalds contributions to software development and technology innovation.

This task should performed in 2 phases.

Phase 1 - Outline, Internal planning.
Identify 3-5 key contributions you believe are most important. For each contribution add one short justification (why it matters) and a confidence tag: High/Medium/Low. Do not include any facts unless you are highly confident they are correct.

Phase 2 - Final answer.
Using only the High/Medium confidence items from Phase 1, write exactly one paragraph of text in English (120-160 words). Style: neutral, factual, informative.

Output format (must follow exactly):

{Phase 2 result}
```

**Example output**

> Linus Torvalds is best known for creating the Linux kernel in 1991, which became the core of the GNU/Linux operating system and now underpins servers, supercomputers, cloud platforms, and billions of embedded and mobile devices. By releasing Linux under the GNU General Public License, Torvalds enabled large-scale collaborative development and helped establish open source as a viable model for critical infrastructure. He later created Git, a distributed version control system designed to support the rapid, parallel development of the Linux kernel; Git has since become the dominant tool for source code management across the software industry. Torvalds also shaped open-source engineering practices through his long‑term role as lead Linux kernel maintainer, promoting rigorous code review, decentralized contribution, and scalable release processes. Together, these contributions have had a lasting influence on software reliability, developer collaboration, and modern computing ecosystems.

**Implications**

1. **Task decomposition**: The task is split into 2 phases, step-by-step instructions should make it easier for the model to follow them.
2. **Usage of a confidence tags** should reduce the possibility that the model includes invented facts in the result paragraph.
3. **Usage of persona and output format** (including the target paragraph count and word count range) are standard best practices.
4. **Phase 1 can still go wrong**: confidence tags don't eliminate the risk of hallucinations, and some important facts may be left out of scope.
5. **Higher token usage and higher response latency** because of a 2-phase approach.
