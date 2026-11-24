# Zero Two

> **A local-first, modular personal AI assistant that evolves from a conversational AI into an intelligent agent.**

Zero Two is an open-source personal AI assistant project designed to progressively gain the ability to **understand, remember, research, use tools, control software, write code, and execute complex tasks**.

The project is being developed incrementally, release by release, with a strong focus on **modularity, privacy, extensibility, and user control**.

---

## 🚀 Vision

Zero Two is not just a chatbot.

The long-term goal is to build a complete personal AI system:

```text
                         ZERO TWO
                            │
                  ┌─────────▼─────────┐
                  │    AI BRAIN       │
                  └─────────┬─────────┘
                            │
       ┌────────────────────┼────────────────────┐
       │                    │                    │
       ▼                    ▼                    ▼
    Memory                Tools               Voice
       │                    │                    │
       ▼                    ▼                    ▼
      RAG              Computer Control      STT / TTS
       │                    │                    │
       └────────────────────┼────────────────────┘
                            │
                    ┌───────▼───────┐
                    │  Model Layer  │
                    └───────┬───────┘
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
          Local           Cloud          Future
          Models          Models        Zero Two
```

The model is only one component.

**Zero Two is the complete system around the model.**

---

# ✨ Planned Capabilities

Zero Two will progressively support:

- 🤖 Conversational AI
- 🧠 Long-term memory
- 🎙️ Voice input
- 🔊 Voice output
- 🌐 Web search
- 🔎 Web research
- 🛠️ Tool execution
- 💻 Computer control
- 📂 File operations
- 📄 Document understanding
- 📚 RAG / personal knowledge
- 👨‍💻 Coding assistance
- 🧩 Skills and plugins
- 🧠 Task planning
- ⚙️ Autonomous task execution
- 🔐 Permission and security controls
- 📊 Execution monitoring
- 🤖 Future customized Zero Two model

---

# 🏗️ Architecture

Zero Two is designed to be **provider-independent**.

```text
User
 │
 ▼
Interface
 │
 ▼
Zero Two Core
 │
 ▼
Orchestrator
 │
 ├───────────────┐
 ▼               ▼
Brain          Memory
 │               │
 ▼               ▼
Model          RAG
Layer
 │
 ├── Local Models
 │
 ├── Cloud Models
 │
 └── Future Zero Two Model
 │
 ▼
Tools / Skills / Plugins
 │
 ├── Computer
 ├── Web
 ├── Files
 ├── Applications
 └── External Services
```

---

# 🧠 Model Independence

Zero Two is **not locked to a single AI provider**.

The architecture is intended to support multiple model backends.

### Local

- Ollama
- llama.cpp
- Transformers
- Other local runtimes

### Cloud

- Groq
- OpenAI
- Google
- Other providers

### Future

- Custom Zero Two model

The model provider can be changed without redesigning the entire assistant.

---

# 🔒 Local-First Philosophy

Privacy and control are major design goals.

Whenever practical, Zero Two should process information locally.

Benefits include:

- Better privacy
- Reduced API costs
- Offline capabilities
- Greater control
- Reduced provider dependency

Cloud AI can still be used when it provides capabilities that local models cannot efficiently provide.

---

# 🖥️ Current Development Hardware

The current development baseline is:

| Component | Specification |
|---|---|
| OS | Windows 11 Home Single Language |
| Architecture | x64 |
| RAM | 16 GB |
| CPU | Intel |
| GPU | Intel UHD Graphics |
| GPU Type | Integrated |
| Initial Target | Local model execution |

The project architecture is hardware-independent and should later support stronger systems, dedicated GPUs, and other operating systems.

---

# 📦 Project Status

**Current Stage:** Planning / v0.1 development

The project is being developed incrementally.

We are intentionally avoiding building every feature at once.

---

# 🗺️ Roadmap

## v0.1.0 — Core

Build the foundation.

- Project architecture
- Configuration
- Model provider abstraction
- Local model integration
- Basic conversation
- CLI
- Logging
- Error handling

**Goal:** A working local Zero Two core.

---

## v0.2.0 — Voice

- Speech-to-text
- Text-to-speech
- Microphone input
- Speaker output
- Voice pipeline

**Goal:** Zero Two can listen and speak.

---

## v0.3.0 — Tools

- Tool framework
- Calculator
- File operations
- System information
- Application launcher
- Basic command execution

**Goal:** Zero Two can perform useful actions.

---

## v0.4.0 — Computer Control

- Application control
- Mouse interaction
- Keyboard interaction
- Window management
- Desktop automation

**Goal:** Zero Two can interact with the computer.

---

## v0.5.0 — Web

- Web search
- Page retrieval
- Research
- Source comparison
- Citations

**Goal:** Zero Two can research current information.

---

## v0.6.0 — Memory

- Long-term memory
- User preferences
- Memory retrieval
- Memory management
- Forget/delete functionality

**Goal:** Zero Two remembers useful information.

---

## v0.7.0 — RAG

- Document ingestion
- Embeddings
- Vector storage
- Retrieval
- Personal knowledge base

**Goal:** Zero Two understands the user's documents.

---

## v0.8.0 — Coding Agent

- Repository analysis
- Code generation
- Code modification
- Testing
- Debugging
- Development workflows

**Goal:** Zero Two becomes a development assistant.

---

## v0.9.0 — Autonomous Agent

- Task planning
- Multi-step execution
- Task state
- Retries
- Verification
- Human approval checkpoints

**Goal:** Zero Two can complete complex tasks.

---

## v1.0.0 — Full Zero Two

Combine:

- Voice
- Brain
- Tools
- Computer control
- Web
- Memory
- RAG
- Coding
- Autonomous execution
- Security
- UI

**Goal:** A practical personal AI operating layer.

---

## v1.x — Zero Two Model

Future research direction:

```text
Open Model
    ↓
Zero Two Dataset
    ↓
Prompt / Instruction Tuning
    ↓
Fine-Tuning
    ↓
Zero Two Specialized Model
    ↓
Optimization
```

The initial project will **not** attempt to train a GPT-scale model from scratch.

The first priority is building the assistant platform and collecting the infrastructure and data required for future model development.

---

# 📁 Planned Project Structure

The repository will evolve over time, but the initial architecture is expected to follow a structure similar to:

```text
Zero-Two/
│
├── app/
│   ├── core/
│   ├── brain/
│   ├── models/
│   ├── tools/
│   └── main.py
│
├── tests/
│
├── docs/
│
├── scripts/
│
├── .env.example
├── .gitignore
├── README.md
├── CHANGELOG.md
├── LICENSE
└── pyproject.toml
```

The structure may change as the architecture matures.

---

# 🛡️ Security

Security is a core requirement.

Zero Two should not blindly execute potentially dangerous actions.

The long-term execution pipeline is:

```text
User Request
     ↓
Intent
     ↓
Permission Check
     ↓
Tool Validation
     ↓
Execution
     ↓
Verification
```

Potentially dangerous operations may require explicit confirmation.

Examples:

```text
Delete files
Send messages
Send emails
Purchase items
Modify system settings
Execute unknown programs
```

---

# 🔐 Privacy

Zero Two follows a local-first approach.

Important principles:

- Do not hardcode API keys.
- Keep sensitive data local whenever practical.
- Avoid unnecessary data transmission.
- Provide user control over stored memory.
- Avoid unnecessary sensitive information in logs.
- Make external API usage transparent.

---

# 🧩 Extensibility

Zero Two is intended to support a future plugin and skills ecosystem.

Example:

```text
Plugin
├── Manifest
├── Description
├── Permissions
├── Tools
├── Configuration
└── Execution
```

Possible future integrations:

- GitHub
- Gmail
- Calendar
- Discord
- Slack
- Notion
- Spotify
- Browser
- Development tools

---

# 🧪 Development Philosophy

Zero Two is being built **release by release**.

Each release should provide a stable foundation for the next one.

We will prioritize:

- Clean architecture
- Small dependencies
- Testing
- Documentation
- Security
- Reproducibility
- Maintainability
- Extensibility

A feature will not be considered complete simply because the code works.

---

# 📋 Definition of Done

Each release should include:

- Working implementation
- Tests
- Documentation
- Configuration example
- Error handling
- README updates
- Changelog entry
- Version number
- Git tag
- Release notes
- Basic security review

---

# 📌 Current Milestone

## v0.1.0 — Zero Two Core

The immediate objective is to build:

```text
User
 ↓
Zero Two CLI
 ↓
Core
 ↓
Brain
 ↓
Model Provider
 ↓
Local Model
 ↓
Response
```

The first version should establish the architecture that all future versions will build upon.

---

# 🤝 Contributing

Contribution guidelines will be added as the project opens for broader collaboration.

Potential contribution areas include:

- Core architecture
- Model providers
- Voice
- Tools
- Memory
- RAG
- UI
- Computer control
- Security
- Testing
- Documentation

---

# 📜 License

License information will be added when the project's licensing strategy is finalized.

---

# 📚 Documentation

Detailed product requirements are maintained separately in:

```text
docs/PRD.md
```

The PRD contains the detailed product vision, architecture, requirements, roadmap, and long-term direction.

---

# ⭐ Project Philosophy

> **The goal is not to build a flashy AI demo.**
>
> **The goal is to build a foundation that can evolve into a serious personal AI system.**

Zero Two will start small.

It will become smarter through architecture, tools, memory, data, and continuous development.

```text
v0.1  → Core
  ↓
v0.2  → Voice
  ↓
v0.3  → Tools
  ↓
v0.4  → Computer
  ↓
v0.5  → Web
  ↓
v0.6  → Memory
  ↓
v0.7  → RAG
  ↓
v0.8  → Coding
  ↓
v0.9  → Autonomy
  ↓
v1.0  → ZERO TWO
  ↓
v1.x  → ZERO TWO MODEL
```

**Project Zero Two — Build the assistant, not just the chatbot.**
