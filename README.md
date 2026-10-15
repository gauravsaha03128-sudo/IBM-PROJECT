# AI Saksham — Personalized Learning Assistant

AI Saksham is a responsive educational web app prototype aligned with **SDG 4: Quality Education**. It demonstrates personalized lessons, English/Hindi explanations, topic-based quizzes, answer feedback, and local progress tracking.

## Features

- **Lesson studio:** Mathematics, Science, and English topics.
- **Learning levels:** Beginner, Standard, and Quick Revision.
- **English/Hindi support:** switch explanations and quiz feedback between English and Hindi.
- **Practice quizzes:** five multiple-choice questions per topic, instant feedback, and score tracking.
- **Progress dashboard:** lessons understood, questions answered, accuracy, and recent quiz history.
- **Local persistence:** saves progress in the browser using `localStorage`.
- **Responsive UI:** desktop, tablet, and mobile layouts.
- **Dark mode:** theme preference is saved locally.
- **No API key required:** works as a static site and can be hosted on GitHub Pages.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a browser.

For a more realistic local web server, you can use VS Code's **Live Server** extension or run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

The site is published at <https://gauravsaha03128-sudo.github.io/IBM-PROJECT/>.

The GitHub Actions workflow in `.github/workflows/deploy-pages.yml` deploys the site automatically whenever changes are pushed to `main`. For the initial setup, enable **Settings → Pages → Build and deployment → Source: GitHub Actions** in the repository.

## Project structure

```text
ai-saksham/
├── index.html     # App structure and sections
├── style.css      # Responsive design and dark mode
├── app.js         # Lesson content, quizzes, scoring, and saved progress
└── README.md      # Setup and deployment guide
```

## Important project scope

This is a **working front-end prototype**, not a live generative-AI service. Lesson explanations and quizzes come from curated sample content in `app.js`; “personalization” currently means selecting a learning level, language, and topic and receiving topic-specific practice. No user data is sent to a server; progress stays in the current browser.

### How to add a live AI model later

A production version should use a backend API (for example, Python + FastAPI) to call an AI provider securely. Never put a private API key in `app.js` or any code shipped to GitHub Pages. Add authentication, rate limits, content moderation, teacher review, and age-appropriate privacy controls before collecting real student information.
