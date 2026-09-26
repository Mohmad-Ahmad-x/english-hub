# English HUB + Rawan English Specialist

Rawan is connected through a secure Node.js backend to Groq using `openai/gpt-oss-120b`. This version expands her role into a broad English-language tutor covering grammar, vocabulary, translation, writing, pronunciation, reading, listening, usage, corrections, idioms, exam practice, and more.

## Setup
1. Create a Groq API key.
2. Copy `.env.example` to `.env`.
3. Put your key in `.env`:

```env
GROQ_API_KEY=gsk_your_real_key_here
PORT=3000
```

4. Install and run:

```bash
npm install
npm start
```

Open `http://localhost:3000`. Do not open `index.html` directly because Rawan uses the backend endpoint `/api/rawan`.

## Rawan v2
- Broad English-language specialization
- Arabic, English, and mixed-language explanations
- Grammar, vocabulary, translation, correction, writing, pronunciation/IPA, reading, listening, idioms, phrasal verbs, presentations, and practice
- One-question-at-a-time quiz/practice behavior
- Hint mode without immediately revealing answers
- Changes explanation style when the student does not understand
- Conversation context retained for recent messages
- Medium reasoning for stronger answers while retaining fast Groq inference
- Hidden model reasoning is not returned to the browser

## Security
- `.env` is ignored by Git.
- The API key stays on the server and is never sent to the browser.
- Never commit your real `.env` file.
