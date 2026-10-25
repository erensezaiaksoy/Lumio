# Lumio

Lumio is a free, accessible web app that helps older Vermonters build confidence with everyday technology, understand artificial intelligence, and recognize online scams.

## Features

- Fourteen searchable, categorized lessons with steps and knowledge checks
- Read-aloud support, adjustable text size, high contrast, and reduced motion
- A private, rule-based suspicious-message checker
- Five-question “Scam or safe?” practice challenge
- Family safe-word planning card
- A clearly labeled pretend chatbot for safe AI practice
- Vermont help resources
- Optional email accounts with cross-device lesson and quiz progress
- Guest progress and user-testing feedback stored on the device
- Offline support after the first visit

## Privacy

Lumio can be used without an account. Guest progress, settings, and testing feedback stay in the browser. When a user chooses to sign in, only lesson IDs, quiz score/attempt count, and the account identifier are stored in Supabase. Message-checker text, safe words, chatbot text, settings, and feedback are never uploaded.

## Connect the free Supabase backend

1. Create a Supabase project and open its SQL Editor.
2. Run `supabase-schema.sql` to create the progress table and per-user security policies.
3. In Authentication settings, keep email/password enabled. Add the deployed Lumio URL and local URL (for example `http://localhost:8000`) to the allowed redirect URLs.
4. Copy `config.example.js` to `config.js`, then add the project URL and **anon/public** key from Project Settings > API. Never use the service-role key in this browser app.

`config.js` is ignored by Git. For static hosting, create it during deployment from the host's environment variables, or store the public URL and anon key in the hosting provider's configuration. Supabase anon keys are designed to be public; row-level security is what protects user data.

## Run locally

Serve this folder with any local web server. For example:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Technology

Lumio uses plain HTML, CSS, and JavaScript. It has no framework, build step, or paid service, so it can be hosted directly with GitHub Pages.

## Congressional App Challenge disclosure

This project was developed with assistance from generative AI. The student should replace this paragraph with an accurate first-person description of which ideas, text, code, debugging, testing, and revisions were completed by the student and which were assisted by AI before submitting.

## License

This project is intended for educational use.
