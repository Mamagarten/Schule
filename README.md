# Schule
All about Schule: Klassengeld, Vocab apps, and other tools to facilitate school purposes.

# Klassengeld App


# Vocab app
Google Spreadsheet based vocab trainer.
- Column names: Eng, Deu
- One sheet per chapter/topic/vocab set
- One sheet for points and stats, sheet name "progress", columns: User, Chapter, Eng, Deu, Status (new, in_progress, completed), Attempts, English_Points, German_Points, Last_Updated

Flashcard features:
- Select chapter/topic/set name
- Kids friendly UI, Embed a lightweight CSS/JS frontend (e.g., Tailwind CSS via CDN or vanilla CSS with bright colors, large touch targets, sound effects/animations via Web Audio API)
- Display number of completed, in progress, and new cards
- Prioritize new and in progress cards over completed
- Game Modes:
  1. Learn mode, display card by card
  2. Type the english word - mark as "complete" when correct and add 2 English points for each correct word. If wrong, display correct spelling. .trim().toLowerCase() user input to avoid frustrating kids over trailing spaces or capitalization.
  3. Task is to match to the correct translation. In the left, 10 English words in random order. On the right, 10 respective German translation in random order. Add 1 German point for each correct match. Handle edge cases where a chapter has < 10 total words
- Multiple kids or fast clicks updating points/stats sheet via Apps Script can cause write collisions; batch stats updates or write row-by-row with simple locking.
- Highscore page: per chapter, overall (only English points are rated)
