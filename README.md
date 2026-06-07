# Quiz Master

Quiz Master is a modern, mobile-first Progressive Web Application (PWA) for taking, managing, and reviewing multiple-choice quizzes. All data is processed entirely on your device and saved to your browser's local storage.

## ✨ Features

- **Modern UI/UX**: Premium aesthetic with micro-animations, clean interfaces, and responsive layout optimized for mobile screens.
- **No Backend Required**: 100% offline-ready. Quizzes are stored in your browser's `localStorage`.
- **Multiple Modes**: Play your quiz in Normal mode, Shuffle Answers, or Shuffle Questions & Answers.
- **Save Progress**: Temporarily save your quiz progress and resume later.
- **Smart Review System**: Retake only the questions you got wrong, or review your answers after completing a quiz.
- **PWA Ready**: Can be installed directly to your phone's home screen for a native app experience.

## 🚀 How to Run

1. Since this is a PWA, for the best experience (and to allow PWA installation on mobile), serve the folder using a local web server (e.g., **Live Server** extension in VS Code).
2. Open the URL to `index.html` in your modern web browser.
3. On the Home screen, click the **floating `+` button** at the bottom right to import your quiz file.

## 📂 Importing a Quiz (JSON Format)

The application accepts `.json` files. The **name of the file** (e.g., `my_quiz.json`) will automatically be used as the **Quiz Title** ("my_quiz").

### Required JSON Structure

The JSON file must be an array of objects. Each object represents a single question.

```json
[
  {
    "term": "What is the capital of France?\nA. Berlin\nB. Madrid\nC. Paris\nD. Rome",
    "definition": "C",
    "termImage": null,
    "definitionImage": null
  },
  {
    "term": "Which of these is a valid JavaScript data type?\nA. Float\nB. Boolean\nC. Integer\nD. Character",
    "definition": "B",
    "termImage": null,
    "definitionImage": null
  }
]
```

### Breakdown of Fields:
- **`term`**: A single string containing the question **AND** the options.
  - The question text can span multiple lines.
  - The options must be listed on new lines, starting with an uppercase letter followed by a period or parenthesis and a space (e.g., `A. `, `B) `).
- **`definition`**: A string containing the uppercase letter of the correct answer (e.g., `"A"`, `"B"`, `"C"`, `"D"`).
- `termImage` / `definitionImage`: Ignored by the app but can be left as `null`.

## 📱 Installing on Mobile

1. Host the project directory on a secure server (HTTPS) or run it locally on your network.
2. Open the URL in Chrome (Android) or Safari (iOS).
3. Tap the browser menu and select **Add to Home screen** or **Install App**.
4. The Quiz Master icon will appear on your phone's home screen as a standalone application.
