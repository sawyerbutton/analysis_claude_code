# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a comprehensive reverse engineering analysis of Claude Code v1.0.33. It documents the core architecture, implementation mechanisms, and operational logic discovered through systematic analysis of obfuscated source code.

## Key Directories

- `claude_code_v_1.0.33/stage1_analysis_workspace/` - Main analysis workspace containing all research materials
- `docs/` - Technical documentation including architecture analyses, verification reports, and implementation guides
- `chunks/` - Deobfuscated code chunks (102 files) from the original source
- `scripts/` - Analysis tools for code beautification, splitting, and LLM-assisted analysis
- `work_doc_for_this/` - Project methodology documentation and SOPs

## Development Commands

### Analysis Scripts
```bash
# Code beautification
node claude_code_v_1.0.33/stage1_analysis_workspace/scripts/beautify.js [source_file]

# Split code into chunks
node claude_code_v_1.0.33/stage1_analysis_workspace/scripts/split.js [beautified_file]

# Merge chunks
node claude_code_v_1.0.33/stage1_analysis_workspace/scripts/merge-again.js

# LLM-assisted analysis
node claude_code_v_1.0.33/stage1_analysis_workspace/scripts/learn-chunks.js
```

### Open-Claude-Code Subproject
```bash
cd claude_code_v_1.0.33/stage1_analysis_workspace/docs/Open-Claude-Code/

# Build TypeScript code
npm run build

# Run tests
npm test

# Run benchmarks
npm run benchmark

# Lint code
npm run lint

# Development mode
npm run dev
```

## High-Level Architecture

### Core Technical Discoveries

1. **Real-time Steering Mechanism** - h2A dual-buffer asynchronous message queue enabling zero-latency message passing
2. **Multi-layered Agent Architecture** - Main Agent (nO), SubAgents (I2A), and Task Agents with isolated execution environments
3. **Intelligent Context Management** - Automatic compression at 92% threshold with wU2 compressor
4. **Enhanced Security** - 6-layer permission validation from UI to tool execution

### Key Components

- **nO Agent Loop Engine** - Core orchestrator using async generators
- **h2A Message Queue** - Promise-based asynchronous communication
- **MH1 Tool Engine** - 6-stage tool execution pipeline
- **UH1 Concurrency Controller** - Manages up to 10 concurrent tool executions
- **wU2 Context Compressor** - Smart memory management with 92% threshold

### Repository Focus Areas

1. **Static Code Analysis** - Understanding obfuscated code patterns
2. **Architecture Documentation** - Mapping system components and interactions
3. **Verification Reports** - Cross-validating findings with 95% accuracy
4. **Open Source Reconstruction** - Providing implementation guides for recreating the system

## Important Notes

- This is a research and educational project analyzing obfuscated code
- Analysis accuracy is estimated at 85-95% based on verification methods
- The repository focuses on understanding AI Agent engineering patterns
- Not all findings may be 100% accurate due to code obfuscation complexity