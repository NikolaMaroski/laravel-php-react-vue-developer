# CLAUDE.md

## Project Overview

Senior Developer Interview Prep App — an interactive single-page application for preparing for technical interviews (PHP/Laravel + React + Vue). Modeled after a real interview vetting process with a 1.2% acceptance rate.

## Tech Stack

- **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6+)
- **No build tools, no dependencies** — open `index.html` directly in a browser
- **Single-file SPA:** All code lives in `index.html` (~4,000 lines)

## Architecture

- Mobile-first responsive design with sidebar navigation
- 22 content sections organized by technology (PHP, Laravel, React, Vue, System Design, DevOps)
- Interactive features: quizzes (35 questions), coding challenges (4), mock interview Q&A (10)
- Dark theme with CSS custom properties for theming
- No external API calls — everything runs client-side

## File Structure

```
/
├── index.html        # The entire application
├── README.md         # Project documentation
└── CLAUDE.md         # This file
```

## Key Conventions

- All visible branding uses "Interview.io" — resource links may point to the original source URLs
- CSS uses custom properties (variables) defined in `:root`
- JavaScript is vanilla ES6+ with no transpilation
- Navigation is handled via `data-section` attributes on sidebar links
- Quizzes use `data-correct` attributes on question containers
- Coding challenges use regex-based pattern matching for auto-checking

## Content Sections

### Getting Started
- Overview & Process (interview stages, scoring framework)
- Scoring & What They Want (100-point breakdown)

### PHP 8 Core
- PHP 8 Deep Dive (PHP 5/7/8 differences, new features)
- OOP & Design Patterns (SOLID, Repository, Strategy)
- Security & Performance (SQL injection, XSS, CSRF, optimization)

### Laravel
- Service Container & Providers (binding, singleton, middleware, routing)
- Eloquent & Database (relationships, N+1, scopes, migrations)
- Queues, Events & Jobs (job chaining, batching, observers, scheduling)
- Auth, Policies & Gates (Sanctum, policies vs gates)
- Architecture & Patterns (Action pattern, Form Requests, API Resources, caching, testing)

### React
- Hooks & State (useState, useEffect, useRef, useReducer, Context, custom hooks)
- Advanced Patterns (HOC, render props, compound components, error boundaries)
- Performance & Architecture (memo, code splitting, Virtual DOM, Fiber, SSR)

### Vue
- Composition API & Reactivity (ref vs reactive, watchers, composables)
- Pinia, Router & SSR (Pinia vs Vuex, navigation guards, hydration)

### System Design & DevOps
- System Design (e-commerce example with full architecture walkthrough)
- DevOps & CI/CD (Docker, GitHub Actions, production checklist)

### Practice
- PHP & Laravel Quiz (15 questions)
- React Quiz (10 questions)
- Vue Quiz (10 questions)
- Coding Challenges (4 challenges with hints and solutions)
- Mock Interview Q&A (10 senior-level questions with model answers)
- Resources & Tips (learning links, interview checklist, red flags)

## Development Notes

- To add a new section: add a `<section id="new-id">` in the main div, add a nav link with `data-section="new-id"` in the sidebar
- To add quiz questions: add a `.quiz-q` div with `data-correct="letter"` inside the quiz container
- To add coding challenges: add entry to `challengeChecks` object in the script section
- Git config for this repo uses `NikolaMaroski <nikola.maroski1@gmail.com>`
