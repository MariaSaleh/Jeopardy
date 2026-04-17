# 🏆 Grand Stage Jeopardy Pro

A high-end, multimedia-ready Jeopardy engine designed for live events. This version features automated turn-tracking, a unique **Half-Penalty** system, and a **Live Editable Scoreboard**.

---

## 🕹️ How to Play

### 1. Initial Setup
* **Team Names:** Enter names in the setup overlay. Use the **+ ADD TEAM** button to include as many teams as needed (supports 2 to 6+ teams).
* **Starting:** Click **ENTER STAGE** to generate the board and begin the session.

### 2. Gameplay Mechanics
* **The Active Turn:** One team box at the bottom will always have a **Yellow Glow**. This indicates whose turn it is to choose a card from the board.
* **Card Values:** Each card displays a dollar amount. Clicking it opens the question modal.
* **Multimedia:** If a question contains an image, video, or audio file, it will automatically play or display within the modal above the question text.

### 3. Scoring System
When a question is revealed, you have three ways to adjust the score of the **active team**:
* **CORRECT (+Full):** Adds the full value displayed on the card (e.g., +$200).
* **WRONG (-Half):** Subtracts **50%** of the card's value as a penalty (e.g., -$100).
* **ADD CUSTOM POINTS:** Type a specific number into the "Value" input box and click the nav button. Use a negative number (e.g., `-50`) to subtract a custom amount.

### 4. Direct Score Editing (Live Correction)
If you need to override a score manually or fix a typo during the game:
1.  Click directly on the **Dollar Amount** (e.g., $400) in the team bar.
2.  The `$` sign will temporarily disappear, letting you type a new number.
3.  Click anywhere else on the screen (or press Tab). The game will automatically re-format the text with the `$` sign and update its internal memory.

---

## 🛠️ Modifying Game Content (`game_data.json`)

To change the categories and questions, edit your `game_data.json` file. The engine is designed to handle varying amounts of content.

### JSON Schema Example
```json
{
  "categories": [
    {
      "name": "YOUR CATEGORY",
      "questions": [
        { 
          "q": "What is the question text?", 
          "a": "The Answer",
          "value": 500,
          "image": "q1.jpg",
          "video": "intro.mp4",
          "audio": "clue.mp3"
        }
      ]
    }
  ]
}
