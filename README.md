# QuickFlash

A minimalist flashcard study app built with a single HTML file (embedded CSS and JS) that loads card decks from JSON.

## Features
- Load flashcards from a JSON file
- 3D flip animation for card reveal
- Track "Known" vs "Still Learning" for each card
- Re-study only difficult cards
- Shuffle deck, limit cards, choose starting side (front/back first)
- Dark mode toggle (remembers preference)
- Keyboard shortcuts for efficient studying
- No build tools, no dependencies – just open and go

## Run locally
1. Clone or download this repository
2. Open `QuickFlashJSON.html` in your browser
3. Upload one of the example JSON decks (or your own)

## JSON Format
The app expects an array of card objects. Each card must have:
- `front` (string) – the question/prompt side  
- `back` (string) – the answer side  

Optional fields:
- `hint` (string) – shown on the front side before flipping  

Aliases: `question` / `answer` are also supported.

### Example
```json
[
  {
    "front": "What is the capital of France?",
    "back": "Paris",
    "hint": "City of Light"
  },
  {
    "question": "2 + 2",
    "answer": "4"
  }
]
```

## Project structure
- `QuickFlash.html` – the entire app (UI, styles, logic)
- `examples/` – sample JSON decks to get started

## Keyboard shortcuts

| Key           | Action                   |
|:--------------|:-------------------------|
| ← / →         | Previous / Next card     |
| Space / Enter | Flip card                |
| Y             | Mark as Got it           |
| N             | Mark as Still learning   |

## Notes
This is a small personal project inspired by QuickQuizJSON. The setup is intentionally minimal, perfect for self-hosting, local study, or learning how flashcard UIs work.

>Built with vanilla HTML, CSS, and JavaScript.
