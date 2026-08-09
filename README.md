#  XML LSP ECOSYSTEM

A high-performance, modular XML tooling ecosystem built entirely in TypeScript and WASM. No Java or JVM required.

## System Architecture

flowchart TB
    V["xerces-wasm-validator<br/>(C++ Apache Xerces in WebAssembly)"]
    S["xml-language-service<br/>(Diagnostics, Completion, Formatting, XSD)"]

    V --> S

    S --> L["xml-language-server<br/>(LSP Implementation)"]
    S --> B["xml-review-bot-demo<br/>(GitHub Action)"]

    L --> VS["VS Code Client"]
    L --> M["xml-lsp-marketplace<br/>(Claude Code)"]

    V -.-> P["xerces-playground<br/>(Live Web Browser UI)"]

    classDef core fill:#f6f8fa,stroke:#57606a,color:#24292f
    class V,S,L,B,VS,M,P core

## Ecosystem Repositories

### Core Engines & Validation
