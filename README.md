# AZ Cloud Recall

A study app for the **Microsoft Azure Fundamentals (AZ-900)** exam. Spaced-repetition flashcards, timed practice exams, a service-matching game, handwritten-style notes and progress tracking, in a single self-contained `index.html`.

> Unofficial study aid. Not affiliated with or endorsed by Microsoft. Skills measured follow the AZ-900 study guide dated July 2026. Check Microsoft Learn for changes.

## History

- Started as "Flashcard Coach" (Memory and Revision), narrowed to AZ-900, then named **AZ Cloud Recall**.
- Rebuilt from a basic single-screen app into a multi-page app with a side menu, rank system, doodles and script fonts.

## Pages

| Page | What it does |
| --- | --- |
| Home | Aurora hero, daily goal ring, streak, exam countdown, exam map (three skill areas with weights and mastery), coach's note, due-this-week chart |
| Study | Pick a deck or all decks. 3D flip cards, Again/Hard/Good/Easy grading, optional "type my answer first", undo, keyboard shortcuts |
| Practice Exam | Timed multiple choice. Presets: Sprint (10 q, 10 min), Standard (20 q, 20 min), Full mock (41 q, 45 min). Focus by skill area, timer on or off, flag for review, question navigator, results with per-area scores, answer review and "add missed to flashcards" |
| Service Match | Click-to-pair game linking Azure services to what they do. Timer with a 3 second penalty per miss and a saved best time |
| Library | Create, edit, search and delete decks and cards. Paste-import and copy-export |
| Notes | Sticky notes in a handwriting font, colours, pinning, saved as you type |
| Progress | Readiness gauge, rank and XP, 16-week activity heatmap, 14-day recall chart, mock score trend, badges, cards to rewrite, forgetting-curve illustration, settings |

## Content

- Starter decks follow the three skill areas: Cloud concepts (25-30%), Azure architecture and services (35-40%), Management and governance (30-35%). Extra decks: Acronyms and names, Exam basics. About 110 cards.
- 41 practice questions written for this app (11 cloud concepts, 17 architecture, 13 governance). Not real exam items.
- 34 service and description pairs for the match game.
- A content version number (`PACKV`) lets new starter cards be added to existing users' decks without touching their own cards.

## Scheduling

Simplified SM-2 style. Again returns in 10 minutes and lowers ease. Hard, Good and Easy multiply the interval (Good: 2, 4, then interval x ease days). Cards missed 3 or more times are flagged as leeches.

## Ranks, XP and badges

XP per review: Again 2, Hard 6, Good 10, Easy 12. Mock exams and match rounds add more. Ranks: Page, Squire (150), Knight (450), Baron (1000), Earl (1800), Duke (3000), Cloud Sovereign (5000). Ten badges.

## Design

- Palette: **Deep Teal and Damson**. Transformative Teal and Divine Damson (2026 colours of the year) with a cloud-dancer-inspired white. Light and dark themes via CSS tokens.
- Fonts (Google Fonts): Syne (bold headlines), Pinyon Script (cloudy script accents), Caveat (handwriting), Figtree (body), DM Mono (data).
- Doodles are inline SVG: crown, clouds, sparkles, squiggles, arrows, hand-drawn circles. Clouds drift in the hero. Motion respects `prefers-reduced-motion`.
- Responsive: side menu becomes a slide-in drawer under 900px.

## Saving

Progress saves to the browser (`localStorage`). When hosted as a Claude artifact with the `db` and `user` capabilities, it also syncs to the viewer's private account storage (`data/users/<id>/`).

## Run it

Open `index.html` in a browser. Fonts load from Google Fonts when online and fall back to system fonts offline.

## Ideas for later

Quiz mode per flashcard deck, multi-select exam questions, more match rounds, importable question packs.