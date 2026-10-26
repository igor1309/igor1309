# Igor Malyarov

**iOS Tech Lead @ Business Innovation Co — iFora | Swift Engineer | Building Intelligent Systems**

[![Blog](https://img.shields.io/badge/Blog-igor1309.dev-blue?style=flat-square&logo=safari)](http://igor1309.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-igor1309-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/igor1309/)
[![GitHub](https://img.shields.io/badge/GitHub-igor1309-black?style=flat-square&logo=github)](https://github.com/igor1309)

---

## About Me

I lead iOS development at a bank, build learning products for children, and use agents while studying for a second university degree. Through this work, I am developing an AI SDLC: how to take an idea through to a working result with agents, then keep improving it.

Requirements, specifications, and design decisions are kept independently of the code. This lets me revisit the architecture, change languages, and rebuild a project while preserving what I have learned about the problem. Architectural guardrails and reproducible checks allow multiple agents to work in parallel.

The approach evolves with the projects. I compare models and harnesses on real tasks, develop evals, and examine decisions that did not work out. What helps in one project gets tried in others and incorporated into the shared process.

---

## Showcase

Projects built with AI coding agents, published from my private monorepo with their code and tests.

```mermaid
flowchart TD
  mono[("private monorepo<br/>specs, code, tests, agent settings")] --> pick["each project's showcase settings<br/>pick the files to publish, add its public README"]
  pick --> scan["scan for secrets<br/>and private references"]
  scan --> check["build and test the export<br/>on its own, outside the monorepo"]
  check --> repo(["public repo<br/>code, tests, README, screenshots"])
```

**[RexLab](https://github.com/igor1309/rexlab)** — A dinosaur learning game for children ([play it](https://rexlab.enoa.ai))\
React, TypeScript and Vite, with behaviour specified first in Gherkin (87 feature files) and 130+ Vitest test files. Built with AI coding agents working from those specs and tests.

<a href="https://rexlab.enoa.ai">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/rexlab/home-dark.webp">
    <img src="assets/rexlab/home-light.webp" width="600" alt="RexLab's home screen with its dinosaur games">
  </picture>
</a>

**[FolioTell](https://github.com/igor1309/foliotell)** — An offline iPhone app that reads Markdown and plain-text files aloud\
SwiftUI over Apple speech synthesis, with the playback logic in a separate library of pure reducers and effect handlers, 196 Swift Testing tests, and Maestro flows on the simulator. Built with AI coding agents working from specs and tests.

<p>
  <img src="assets/foliotell/reader.webp" width="200" alt="FolioTell reading a Markdown file">
  <img src="assets/foliotell/playing.webp" width="200" alt="FolioTell playing it aloud">
  <img src="assets/foliotell/ru-dark.webp" width="200" alt="FolioTell reading a Russian poem in dark mode">
</p>

**[Agister](https://github.com/igor1309/agister)** — A Go command-line runner for AI-agent work defined in settings files\
Agents, processes and workflows are settings that compose; every run is resolved before it starts, held to its limits and budget, and recorded whole. Pages: [how a run executes](https://igor1309.dev/agister/run-architecture/) and [how settings resolve](https://igor1309.dev/agister/settings-architecture/).

```mermaid
flowchart TD
  request(["agister run"]) --> resolve["settings/resolve<br/>definitions or a refusal"]
  resolve --> workflow["core/workflow<br/>items in order"]
  workflow --> aCall["core/call · admit<br/>hold, limits, budget"]
  aCall --> wrappers["runtime wrappers<br/>bash · claude-code · codex"]
  wrappers --> supervisor["supervisor"]
  supervisor --> program(["the agent's program"])
  workflow --> runstore[("runstore<br/>record.json · events.jsonl")]
```

**[Agonara](https://github.com/igor1309/agonara)** — A bring-your-own-agent environment for learning programs ([live instance](https://agonara.enoa.ai/learn))\
A curator builds a program of topics, concepts, materials and checks; students read it, answer and see where they are weak. Both point the agent they already use at the same HTTP API that serves the `/learn` and `/admin` web UIs. Node.js and SQLite.

<img src="assets/agonara/learn-quick-check.webp" width="600" alt="An Agonara Quick Check: a student answers a question and sees the result">

---

## Interests & Focus

- 🧩 **System architecture** — clean modular boundaries, async pipelines  
- 🧪 **Test-Driven Development (TDD)** — strict red–green–refactor discipline  
- 🤖 **AI-powered products & tools** — building intelligent systems and workflows  
- 📱 **iOS / SwiftUI development** — elegant and composable architectures  
- 🌱 **Continuous improvement** — readability, maintainability, craftsmanship  

---

## Tech Stack

**Languages & Frameworks**  
Swift • SwiftUI • Combine • UIKit • async/await • Core Data • CloudKit  
Solid fundamentals in architecture and design in the age of AI allow me to work across a wide range of modern stacks (JavaScript, Node.js, Python, Kotlin, etc.).

**Architecture & Patterns**  
Clean Architecture • SOLID Principles • Design Patterns • Dependency Injection • Modular SPM design  

**Tools & Practices**  
Xcode • Git • GitHub Actions • CI/CD automation • Firebase • Cloudflare Tunnels • Code Review & Mentoring  
Primary tool: the terminal, where I work with AI systems, automation, and orchestration.

---

## Projects

Selected current and experimental projects:
- **Synthesis Engine** — inference pipeline for structured analysis and reflection  
- **Ghost-Writer** — Firebase-hosted publishing system for prompt collections  
- **Prompt Garden** — structured prompt distribution & hosting  
- **Writer’s Room** — collaborative AI-assisted writing environment built on multi-agent dialogue protocols  
- **RxViewModel** — async orchestration experiments using composable reducers  
- **Billable Backend** — modular service layer for managing client billing and usage accounting  
- **Ledger** — transaction-oriented foundation for tracking and reconciling financial operations  

Each project examines the balance between **automation**, **composability**, and **human intent**.

---

## Featured Work
**[EssentialGhibli](https://github.com/igor1309/EssentialGhibli)** — Production-grade iOS architecture demonstration
A comprehensive showcase of hyper-modular architecture implementing SOLID principles through strictly decoupled Swift Package targets. Features include:
- **Modular composition** — isolated development, testing, and deployment of UI, API, and Cache layers
- **Parallel build optimization** — intelligent module dependencies reducing build times
- **Extensive TDD coverage** — snapshot testing for UI states, localization, and dark mode
- **Platform-agnostic design** — generic presentation layer enabling cross-platform reuse
- **CI/CD pipeline** — automated testing and deployment via GitHub Actions

This project demonstrates how architectural discipline, proper abstraction boundaries, and TDD methodology combine to create maintainable, testable, and scalable iOS applications.

---

## Team & Mentorship

I approach teamwork through structure, shared principles, and code — built on technical clarity, autonomy, and steady collaboration.

- 🧭 **Intent-driven development** — clear reasoning before execution  
- 🧪 **Strict TDD discipline** — code that proves its own correctness  
- 🧩 **Autonomy through architecture** — empowering teams via modular design  
- 💬 **Constructive review culture** — code reviews as shared learning  
- 🌱 **Continuous learning** — documentation, mentorship, and growth mindset  

---

## Writing

I write at [igor1309.dev](http://igor1309.dev) when I have something worth sharing — mostly about Swift, architecture, and AI-assisted development, drawn from real work.

---

## Connect

- 💬 [Telegram](https://t.me/igor1309)  
- 🔗 [LinkedIn](https://www.linkedin.com/in/igor1309/)  
- 📝 [Blog](http://igor1309.dev)  
- 🧰 [GitHub](https://github.com/igor1309)