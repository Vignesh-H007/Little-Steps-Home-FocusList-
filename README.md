# Little Steps Home (FocusList)

> A narrative-driven, empathy-based task sanctuary built with a pure frontend stack. Guide a lost child across shifting biomes back to their family with every task you accomplish.

---

## Overview

**Little Steps Home** reimagines personal task management by replacing traditional stress-inducing point deductions with an emotional, narrative gamification loop inspired by *Studio Ghibli* and *Sky: Children of the Light*. 

The player’s real-world tasks serve as provisions and compass bearings. Completing tasks clears atmospheric fog and moves a lost wanderer forward across dynamic biomes toward their front door.

---

## Core Features & FAIE Requirements

### 1. Task Creation & Priority Tiers
- **Dynamic Task Addition:** Quick pathway entry with task title validation.
- **Three Priority Levels:**
  - **High (Milestone):** Awards `+25 Steps` and unlocks reflective story journal entries.
  - **Medium (Routine):** Awards `+15 Steps`.
  - **Low (Quick Light):** Awards `+5 Steps` to pierce through the mist.
- Clearly distinguishable color-coded badges (Rose, Amber, and Emerald).

### 2. Task Management (CRUD)
- **Toggle Completion:** Checking off a pathway updates real-time steps and light meters. Re-opening a task cleanly recalculates expedition progress.
- **Inline Editing:** Edit pathway names and change priority levels via a modal dialog.
- **Deletion:** Safely prune pathways from the expedition ledger.

### 3. Search & Multi-Criteria Filtering
- **Real-Time Search:** Instant filtering by task title.
- **Status Filter:** Segment tasks by `All`, `Active`, and `Completed`.
- **Priority Filter:** Isolate tasks by `High`, `Medium`, or `Low` priority.

### 4. Dynamic Task Statistics
- Live counters for **Total Tasks**, **Pending in Fog**, and **Path Cleared**.
- Responsive top expedition bar tracking **Lantern Light (%)**, **Steps Walked**, and **Journal Reflections**.

### 5. Data Persistence
- Built-in `localStorage` persistence saves all tasks, narrative progress, footsteps, and unlocked journal entries across page refreshes.

### 6. Narrative Engine & The Anti-Procrastination "Fog"
- **Empathy-Driven Consequence:** Instead of punitive score drops, unresolved pending tasks cause an atmospheric fog layer (`.fog-layer`) to roll over the world canvas. The child halts progress to wait out the fog until the user tackles a task.
- **Interactive Biome Progression:** Footsteps advance the child across four distinct biomes:
  1. *The Whispering Woods*
  2. *The Clockwork Ruins*
  3. *The Forgotten Coast*
  4. *The Quiet Hearth (Home)*
- **Travel Diary:** High-priority achievements record contextual reflections in the child's illustrated travel journal.
- **First-Time Companion Dialogue:** A story-driven welcome modal introduces the child's plight on the initial visit and securely stores onboarding completion.

---

## Technical Stack

- **Markup & Layout:** Semantic HTML5
- **Styling & Design System:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
- **Typography:** [Google Fonts](https://fonts.google.com/) (`Nunito` for clean, legible UI)
- **Iconography:** [Lucide Icons](https://lucide.dev/) (SVG, zero emoji dependency)
- **Visual Canvas:** Native HTML5 2D Canvas API (Procedural silhouette, lighting gradients, particle physics)
- **State Management & Storage:** Vanilla JavaScript (ES6+) with `localStorage`
- **Architecture:** 100% Frontend-only, single-file architecture (`index.html`)

---

## Project Structure

```text
├── index.html        # Complete self-contained application (HTML, CSS, JS)
└── README.md         # Documentation and evaluation guide
