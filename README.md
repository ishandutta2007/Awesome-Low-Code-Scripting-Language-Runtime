# Awesome-Low-Code-Scripting-Language-Runtime

# Awesome Low-Code Scripting Language & Runtime

> A curated list of top Low-Code Scripting Language and Runtime platforms — both SaaS/Hosted commercial embedded scripting environments and open-source alternatives for extending applications with custom logic without full application rebuilds.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Zoho Deluge](#zoho-deluge)
  - [Google Apps Script](#google-apps-script)
  - [Salesforce Apex](#salesforce-apex)
  - [ServiceNow Flow Designer Scripts](#servicenow-flow-designer-scripts)
  - [Retool JavaScript Runtime](#retool-javascript-runtime)
  - [Appsmith JS Objects](#appsmith-js-objects)
  - [Zapier Code](#zapier-code)
  - [Make Custom Functions](#make-custom-functions)
  - [Workato Recipes](#workato-recipes)
  - [Quickbase Pipelines (Jinja)](#quickbase-pipelines-jinja)
- [Open-Source Software](#-open-source-software)
  - [Windmill](#windmill)
  - [ByteChef](#bytechef)
  - [MEL Agent](#mel-agent)
  - [Weblang](#weblang)
  - [MEvento](#mevento)
  - [Noct](#noct)
  - [D4rt](#d4rt)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Low-Code Scripting Language and Runtime platforms. These are not open-source but are included as reference points for feature comparison.

### Zoho Deluge
**Type:** Scripting language across the Zoho suite
Deluge (Data Enriched Language for the Universal Grid Environment) is Zoho's proprietary scripting language used across Zoho CRM, Cliq, Billing, SalesIQ, and other products to automate workflows, integrate with third-party APIs, and build widgets and bots [citation:1][citation:11]. It is dynamically typed, with data types including Text, Number, Decimal, Boolean, Date-Time, List, Key-Value, and File [citation:1]. Deluge supports `try-catch` blocks for runtime error handling, `throw` for validation failures, and `info` statements for logging [citation:1]. CRM context is central: `zoho.crm.getRecord` returns a Key-Value map, and `zoho.crm.v8.searchRecords` returns a List of Key-Value maps [citation:1].  
**Best for:** Organizations already standardized on Zoho products wanting to extend functionality without leaving the ecosystem, accepting the proprietary lock-in.

### Google Apps Script
**Type:** JavaScript runtime for Google Workspace automation
Google Apps Script is a rapid application development platform for creating business applications that integrate with Google Workspace using modern JavaScript and built-in libraries [citation:2]. Scripts are written in a browser-based editor, saved to Google Drive, and run on Google's servers with no installation required [citation:2]. It can add custom menus, dialogs, and sidebars to Docs, Sheets, and Forms; write custom functions and macros for Sheets; publish web apps; and interact with Gmail, Calendar, Drive, and other Google services [citation:2].  
**Best for:** Teams in the Google Workspace ecosystem wanting to automate workflows and build lightweight add-ons with familiar JavaScript, accepting the Google-only runtime.

### Salesforce Apex
**Type:** Strongly typed, multitenant programming language
Apex is a strongly typed, object-oriented programming language that allows developers to execute flow and transaction control statements on Salesforce servers in conjunction with API calls [citation:3][citation:13]. Its syntax resembles Java and acts like database stored procedures, enabling developers to add business logic to system events including button clicks, record updates, and Visualforce pages [citation:3]. Apex is multitenant-aware, with a runtime engine designed to guard against runaway code monopolizing shared resources [citation:3]. It includes built-in DML calls, inline SOQL/SOSL queries, and unit test support with code coverage reporting [citation:3].  
**Best for:** Salesforce developers needing server-side business logic tightly integrated with the platform's data model, accepting the platform-specific language and governor limits.

### ServiceNow Flow Designer Scripts
**Type:** Server-side scripting within Flow Designer actions
ServiceNow Flow Designer does **not** have an out-of-the-box Script Action . To use scripting, you must create a **Custom Action** with Action Type: Script, where you write server-side logic, then invoke that action inside a Flow . This allows reusable script steps to be called from multiple flows.  
**Best for:** ServiceNow administrators needing server-side logic within flows, accepting that scripting requires custom action creation rather than inline flow scripting.

### Retool JavaScript Runtime
**Type:** JavaScript code blocks within workflows and apps
Retool uses JavaScript as the primary method for manipulating and transforming data, with Code blocks that can transform data and perform complex logic [citation:6]. Preloaded libraries include Lodash, Moment.js, UUID, Numbro, PapaParse, and i18next [citation:6]. Built-in libraries can be added from a library tab, including axios, crypto-js, AWS SDK, and others [citation:6]. Secrets can be accessed via `retoolContext.secrets` on self-hosted instances [citation:6].  
**Best for:** Teams already using Retool for internal tools wanting to extend logic with JavaScript, accepting the platform dependency.

### Appsmith JS Objects
**Type:** JavaScript objects with configurable run behavior
Appsmith's JS Objects support three run behaviors: **Manual** (executes only when explicitly invoked via widget events or JS calls), **On page load** (executes once when the page loads), and **Automatic** (executes whenever referenced variables or inputs change) [citation:7]. Automatic mode tracks all references inside the function and re-runs when any value updates, eliminating manual binding to widget events [citation:7].  
**Best for:** Appsmith users wanting reactive JavaScript logic tied to widget state, accepting the platform's execution model.

### Zapier Code
**Type:** JavaScript or Python code steps in Zap workflows
Code by Zapier lets you run custom JavaScript (Node.js 22) or Python (3.13) as steps in Zaps [citation:8]. Code steps work as both triggers and actions, and action steps can use the Zapier SDK to call other apps and install packages from npm or PyPI [citation:8]. Runtime limits vary by plan: Free (1 second, 512 MB), Professional/Team (30 seconds), Enterprise (2 minutes), with extended runtimes up to 10 minutes for actions on paid plans [citation:8]. Authenticated API calls use the Zapier SDK rather than storing secrets in code [citation:8].  
**Best for:** Zapier users needing custom data transformation or API calls beyond built-in actions, accepting the runtime timeouts and plan-based limits.

### Make Custom Functions
**Type:** Reusable functions within Make scenarios
Make's Custom Functions allow technical users to build functions that manipulate and transform data in complex ways, with testing and debugging in a single view, and enable non-technical users to reuse pre-built functions without writing code [citation:9]. Use cases include payroll scheduling on business days, date validation, type checking, UTM parameter extraction, tax calculation, and duplicate detection [citation:9]. Custom functions are available on the Enterprise plan.  
**Best for:** Make Enterprise users wanting reusable logic across scenarios, accepting the Enterprise plan requirement.

### Workato Recipes
**Type:** Workflow recipes with triggers, actions, and logic
Workato recipes are automated workflows with a trigger and one or more actions, using connectors to integrate with apps [citation:10]. Recipes support conditional logic, loops, and error handling [citation:10]. Types include **Workflow recipes** (most common), **API recipes** (expose endpoints), **Data pipeline recipes** (private preview, ETL/ELT), **App event recipes** (send events to a genie), and **Knowledge base recipes** (sync documents for a genie) [citation:10]. Recipe Copilot uses LLMs to assist with recipe building [citation:10].  
**Best for:** Workato users wanting AI-assisted recipe development with multiple recipe types for different automation patterns.

### Quickbase Pipelines (Jinja)
**Type:** Jinja templating for data transformation in Pipelines
Quickbase Pipelines uses the Jinja programming language to write formulas for math, text manipulation, boolean expressions, date handling, and aggregation from search/query steps [citation:5]. Jinja is ideal for lightweight operations like sending summary emails of the first 100 records, performing conditional logic on a subset, or creating compact dashboards [citation:15]. **Limitation:** Only the first 100 records are accessible with Jinja; for more, use a loop step [citation:15].  
**Best for:** Quickbase users wanting lightweight data transformation within Pipelines, accepting the 100-record Jinja limit.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Low-Code Scripting Language and Runtime tools. The open-source ecosystem spans **polyglot workflow platforms**, **embeddable scripting languages**, and **visual automation platforms with code steps**.

### Windmill
**Stack:** Rust / TypeScript / Python / Go / Bash / SQL | **License:** Apache-2.0 (open-source)
Windmill is an open-source workflow engine and developer platform positioned as an alternative to Retool, Superblocks, n8n, Airflow, and Temporal [citation:22]. Its key differentiator is that you write **real code** in TypeScript, Python, Go, Bash, SQL, or any language, and Windmill instantly exposes that code as APIs, scheduled jobs, workflows, and UIs [citation:17][citation:22]. It includes a **Flow Builder** for composing scripts into DAG workflows with retries and error handling, a **low-code App Builder** for drag-and-drop internal tools, and a **full-code app builder** for React or Svelte frontends [citation:22]. It supports self-hosting with Docker Compose or Kubernetes, with 300+ pre-built resource types and OAuth connectors .  
**Best for:** Developer teams wanting a script-first platform that auto-generates UIs and APIs from their code, accepting the polyglot runtime and self-hosting requirements.

### ByteChef
**Stack:** Java / JavaScript / Python | **License:** Apache-2.0
ByteChef is an open-source platform for building and running workflow automations and AI agents across applications, APIs, and databases [citation:25]. It provides a visual editor with a library of **270+ connectors**, and allows adding **code steps in JavaScript, Python, or Java** where a connector is not enough [citation:25]. AI agents are first-class workflow steps that can be given models, tools, memory, and guardrails, with human approval checkpoints. The same engine can be embedded in your own product [citation:25].  
**Best for:** Teams wanting a visual workflow builder with code steps and embedded integration capabilities, accepting the Java-based self-hosted deployment.

### MEL Agent
**Stack:** Go / React / PostgreSQL | **License:** Open Source (Go package)
MEL Agent is an AI-first workflow automation platform with a visual workflow builder inspired by n8n, Make.com, and Node-RED, built from the ground up for LLM orchestration [citation:18]. Key features include real-time debugging with step-by-step execution traces, live data preview for every node, AI nodes (LLM chat, embeddings), integration nodes (Slack, Baserow, webhooks, HTTP), logic nodes, and a dual worker model (embedded + distributed) for scaling [citation:18]. It is API-first with everything available via REST API.  
**Best for:** Teams building AI-powered workflows wanting a visual builder designed for LLM orchestration, accepting a newer project than Windmill.

### Weblang
**Stack:** JavaScript / YAML | **License:** MIT
Weblang is a low-code programming language for writing safe, portable, and efficient code with minimal logic, designed to let users run code on your server [citation:16]. It is **JSON-compatible** (write in YAML syntax), with file and network access prohibited by default for safety [citation:16]. The runtime is extendable with custom commands (`@db: user/create`), making it suitable for embedding in applications where users supply logic [citation:16]. Variables are dynamic-typed and global, with `@if`/`@then`/`@else` for minimal logic [citation:16].  
**Best for:** Developers embedding a sandboxed scripting language in their applications where users supply custom logic, accepting the minimal language feature set.

### MEvento
**Stack:** JavaScript / TypeScript | **License:** Open Source (npm)
MEvento is an embeddable C-like scripting language and virtual machine for JavaScript and TypeScript host applications [citation:26]. The host keeps control of native behavior by exposing functions, while scripts stored in a database or loaded at runtime compose those functions without rebuilding the host [citation:26]. It supports dot property access, `_try_` result capture, function specs with arity and type hints, script manifest validation, trace mode, and execution step budgets [citation:26]. It has no user-defined functions or classes—the host owns the real logic [citation:26].  
**Best for:** JavaScript/TypeScript developers wanting a small embeddable scripting VM for user-supplied logic, accepting the minimal language scope.

### Noct
**Stack:** C89 | **License:** zlib
Noct is a lightweight, embeddable scripting language written in C89 with a fast JIT compiler and a small runtime (~200 KB), plus an AOT compiler and generational garbage collector [citation:19]. It features C/JS-like syntax, portability across x86, ARM, RISC-V, MIPS, and PowerPC, dictionary-based OOP, and AOT translation to C for platforms where JIT is restricted (iOS, Android, Wasm) [citation:19]. It is designed for embedding in applications like Playfield Engine and Suika3 [citation:19].  
**Best for:** C developers wanting a tiny embeddable scripting language with JIT performance and AOT fallback, accepting the early-stage ecosystem.

### D4rt
**Stack:** Dart | **License:** Open Source (GitHub)
D4rt is a sandboxed Dart interpreter and ecosystem for embedding a scripting engine in Dart or Flutter applications, letting users (or an LLM) supply Dart code that the app evaluates safely at runtime [citation:24]. It includes a bridge generator for native libraries, a REPL/CLI (`dcli`), Flutter integration for rendering UIs from source at runtime, and both source-based (analyzer) and analyzer-free (mirror AST) execution families [citation:24].  
**Best for:** Dart/Flutter developers wanting to embed a Dart scripting runtime with sandboxing, accepting the Dart-specific ecosystem.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Embeddable | Visual Builder | Self-Hosted | Best For |
|----------|---------|-------|------------|----------------|-------------|----------|
| **Zoho Deluge** | Proprietary | Cloud | ❌ | (Widgets) | ❌ | Zoho ecosystem automation |
| **Google Apps Script** | Proprietary | Cloud | ❌ | ❌ (Code editor) | ❌ | Google Workspace automation |
| **Salesforce Apex** | Proprietary | Cloud | ❌ | ❌ | ❌ | Salesforce server-side logic |
| **Retool JS** | Proprietary | Cloud | ❌ | ✅ Code blocks | (Self-hosted) | Retool internal tools |
| **Appsmith JS Objects** | Proprietary | Cloud | ❌ | ✅ JS objects | (Self-hosted) | Appsmith reactive logic |
| **Windmill** | Apache-2.0 | Rust/TS/Python | ❌ (Platform) | ✅ Flow + App | ✅ | Script-first polyglot platform |
| **ByteChef** | Apache-2.0 | Java/JS/Python | ✅ (Embed) | ✅ Visual + code | ✅ | Visual workflows + code steps |
| **MEL Agent** | Open Source | Go/React | ❌ (Platform) | ✅ Node-based | ✅ | AI-first visual workflows |
| **Weblang** | MIT | JavaScript/YAML | ✅ | ❌ | ✅ (Runtime) | Sandboxed user scripting |
| **MEvento** | Open Source | JS/TS | ✅ | ❌ | ✅ (VM) | Embeddable C-like VM |
| **Noct** | zlib | C89 | ✅ | ❌ | ✅ (VM) | Tiny JIT scripting in C |
| **D4rt** | Open Source | Dart | ✅ | ❌ | ✅ (Runtime) | Dart/Flutter embedding |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Low-Code Scripting Language or Runtime tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The open-source landscape for **low-code scripting runtimes** splits between **full workflow platforms** (Windmill, ByteChef, MEL Agent) that combine visual builders with code execution, and **embeddable scripting VMs** (Weblang, MEvento, Noct, D4rt) designed to run user-supplied logic safely inside host applications. **Windmill** is the strongest choice for teams wanting a script-first platform where code auto-generates UIs and APIs [citation:22]. **ByteChef** offers the most embeddable visual workflow engine with 270+ connectors and code steps in multiple languages [citation:25]. For embedding, **Weblang** provides a safe, JSON-compatible YAML-syntax runtime with network/file access disabled by default [citation:16], **MEvento** offers a minimal C-like VM for JS/TS hosts [citation:26], and **Noct** provides a tiny C89 JIT compiler for performance-sensitive embedding [citation:19]. No open-source project replicates the deep platform integration of Deluge or Apex, but these tools cover the core scripting and runtime needs for self-hosted and embedded use cases.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
