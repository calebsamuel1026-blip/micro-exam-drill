# Micro Exam Drill

A single-file study site for microeconomics (Homeworks 7 to 10): drills, timed practice exams and a study guide, with progress saved under a name you type.

Live: **https://calebsamuel1026-blip.github.io/micro-exam-drill/**

## Why

Rereading notes before an exam feels productive but doesn't show what you actually don't know. This site turns the course material (production and costs, perfect competition, monopoly, monopolistic competition and oligopoly) into short question batches, keeps track of every miss, and brings weak topics back until they stick.

## How it works

- Everything is one `index.html`: the question bank, the UI and the logic, with no build step and no framework.
- Tabs: Drill, Practice exam, Progress, Study guide.
- **Drill** serves questions in batches, mixes in spaced-review questions from topics you already know, and offers a "drill my weak spots" round from your misses.
- **Practice exam** is timed and graded at the end, with a per-question review.
- **Progress** shows mastery by topic.
- Progress is stored in `localStorage` and synced through two Supabase RPC functions (load and save) keyed by the name you type, so the same name on another device picks up where you left off. The Supabase key in the page is the public anon key.
- Graph figures used by the questions live in `figs/`.

## Tech stack

HTML, CSS and vanilla JavaScript in one file, Supabase (Postgres RPC) for progress sync, GitHub Pages hosting.

## Run locally

```bash
python -m http.server 8000   # then open http://localhost:8000
```

Or open `index.html` directly in a browser.
