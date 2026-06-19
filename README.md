# Claude Clone — React + Node

A pixel-perfect duplicate of the Claude.ai chat UI, powered by the real Anthropic API.

## Project Structure

```
claude-clone/
├── backend/          ← Node.js + Express API
│   ├── server.js
│   └── package.json
└── frontend/         ← React UI (Claude look-alike)
    ├── src/
    │   ├── App.js
    │   ├── App.css
    │   └── index.js
    ├── public/
    │   └── index.html
    └── package.json
```

## Setup & Run

### 1. Backend

```bash
cd backend
npm install
node server.js
# Runs on http://localhost:3001
```

> The backend reads `ANTHROPIC_API_KEY` from the environment.
> Set it before starting: `export ANTHROPIC_API_KEY=your_key_here`

### 2. Frontend

```bash
cd frontend
npm install
npm start
# Runs on http://localhost:3000
```

The frontend proxies `/api/*` to `localhost:3001` automatically.

## Features

- Dark Claude UI — sidebar, model selector, welcome screen
- Typing animation while waiting for a response
- Markdown rendering (bold, italic, headers, lists)
- Suggestion chips to try ("Tell me about broccoli", etc.)
- Multi-turn conversation memory
- Fully powered by `claude-sonnet-4-20250514`

## Try It

Ask anything! For example:
- "Tell me about tomatoes"
- "What are the benefits of spinach?"
- "Explain how photosynthesis works"
