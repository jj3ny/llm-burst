# llm-burst

A tool for burst processing with LLMs - orchestrating multiple AI chat sessions simultaneously.

## Overview

`llm-burst` replaces complex Keyboard Maestro macros with a simple Python CLI tool that:
- Opens and manages multiple LLM chat sessions (Gemini, Claude, ChatGPT, Grok)
- Arranges windows using Rectangle hotkeys
- Supports tab grouping in Chrome
- Maintains state across sessions

## Project Status

### ✅ Stage 0 - Patch Selectors (Complete)
- Extracted JavaScript selectors from KM macros
- Wrapped selectors in `tryFind()` helpers
- Created Python site modules for all LLMs
- Added basic Playwright tests
- Set up GitHub Actions CI

### 🔲 Stage 1 - swiftDialog Prompt
- Add swiftDialog UI for task name and options

### 🔲 Stage 2 - Chrome Adapter
- Implement Chrome automation via Playwright
- Update state management to record browser/tab IDs

### 🔲 Stage 3 - llm-burst CLI
- Create Python CLI with Click
- Replace KM orchestration with Python

### 🔲 Stage 4 - Auto-naming
- Add Gemini Flash integration for automatic session naming

### 🔲 Stage 5 - Group/UnGroup
- Implement Chrome tab grouping functionality

## Installation

```bash
# Clone the repository
git clone https://github.com/jj3ny/llm-burst.git
cd llm-burst

# Install dependencies
pip install -r requirements.txt

# Install Playwright browsers
python -m playwright install chromium
```

## Testing

```bash
# Run tests
pytest -v

# Run tests with headed browser (for debugging)
pytest -v --headed
```

## Development

See [docs/spec.md](docs/spec.md) for the full technical specification.

## License

MIT