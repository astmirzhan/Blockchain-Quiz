<div align="center">

<img src="docs/screenshot.jpg" alt="Blockchain Quiz home screen: mock exam, parts, open-answer training and choice-only sets" width="100%" />

# ⛓️ Blockchain Quiz

**An exam-prep quiz I built for the Blockchain course final exam: 108 exam questions, a mock exam and free-text answers graded by keywords.**

<p align="center">
  <a href="https://blockchain-quiz-mu.vercel.app"><img src="https://img.shields.io/badge/▶_Open_the_quiz-blockchain--quiz--mu.vercel.app-2563EB?style=for-the-badge&labelColor=1E293B" alt="Open the quiz" /></a>
  <img src="https://img.shields.io/badge/Status-Archived_·_exam_done-64748B?style=for-the-badge" alt="Archived" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML-single_file-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML" />
  <img src="https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Vanilla JavaScript" />
  <img src="https://img.shields.io/badge/Build-none-0EA5E9?style=for-the-badge" alt="No build step" />
  <img src="https://img.shields.io/badge/Vercel-Deployed-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
</p>

</div>

---

## 🎯 What's inside

| | |
| --- | --- |
| **Questions** | 108 in total, split into parts A–E |
| **Question types** | Single choice, multiple choice and written answers |
| **Choice questions** | 72 |
| **Written answers** | 36, grouped into short, medium and long |

| Set | What it is |
| --- | --- |
| 🎯 **Mock exam** | ~42 random questions worth ~100 points, 50% to pass, always in Exam mode |
| 📚 **Parts** | Any single part, or 🔥 all parts mixed together |
| ✍️ **Open-answer training** | Only written questions, by answer length |
| ☑️ **Choice only** | Every single and multiple choice question, no free text |

## 🔁 Two modes

```mermaid
%%{init: {"theme": "base", "themeVariables": {"primaryColor": "#F1F5F9", "primaryTextColor": "#0F172A", "primaryBorderColor": "#2563EB", "lineColor": "#334155", "fontFamily": "monospace"}}}%%
flowchart LR
  S["Pick a set"] --> M{"Mode"}
  M -->|Practice| P["Answer → Check<br/>✓ Correct · ◐ Partial · ✗ Incorrect"] --> N["Next question"] --> P
  M -->|Exam| E["Answer → Submit<br/>no feedback"] --> E
  N --> R["📊 Results"]
  E --> R
```

- **Practice**: instant feedback after every question, with the points you got.
- **Exam**: no hints until the end; 80% to pass (50% for the mock exam).

## 🧮 How answers are scored

| Type | Scoring |
| --- | --- |
| Single choice | 1 point for the right option |
| Multiple choice | +1 for each right option, −1 for each wrong one, never below 0 |
| Written answer | Keyword matching against the model answer, worth the `[N]` points shown in the question |

Written answers are forgiving on purpose: words are stemmed (`ies → y`, `-ing`, `-ed`, `-s`), common stop words
are ignored, and a typo of one letter is accepted in words of 4+ characters (Levenshtein distance ≤ 1).

## 🛠️ Run it

No build step and no dependencies: open `index.html` in a browser, or serve the folder with any static server.
Questions live in `questions.json` (and `questions.js` for opening the file directly).

```bash
npx serve .
```

<div align="center">

**Blockchain Quiz** · built for one exam, kept for the next student 📝

</div>
