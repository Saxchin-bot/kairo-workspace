[kairo_workspace_readme.md](https://github.com/user-attachments/files/34436355/kairo_workspace_readme.md)
# kairo-workspace# KAIRO // WORKSPACE ⏱️

A dynamic, 3-page study block manager and Pomodoro workspace. Built to optimize focus sessions with custom time blocks, integrated task management, and persistent analytics.

**[🔴 View Live Demo Here](https://Saxchin-bot.github.io/kairo-workspace/)** 
*(Deployed via GitHub Pages)*

---

## 📋 Project Overview

This project was built to satisfy the dynamic web application assignment requirements. It features a complete 3-page architecture that feels like a Single Page Application (SPA) by utilizing shared CSS design systems, URL parameter routing, and Web Storage API (`localStorage`) for a database-free backend.

### Core Architecture
* **Frontend:** HTML5, CSS3 (Custom Variables, CSS Grid/Flexbox), Vanilla JavaScript (ES6+).
* **State Management:** `localStorage` acts as the relational database, persistently syncing study blocks, task lists, and focus telemetry across all three pages.
* **Routing:** Dynamic data handoff using `URLSearchParams` allows the Focus Room to load block-specific contexts without needing a backend server.

---

## 🚀 Features by Page

### 1. Dashboard (`index.html`)
* **Live Time Engine:** 24-hour tabular clock with dynamic time-of-day greetings.
* **Active Window Detection:** JavaScript compares the live clock against saved block arrays to automatically highlight currently active study sessions.
* **Block Creator:** A form to generate custom study blocks (e.g., Morning Core, Night Revision) that instantly saves to browser storage.

### 2. Focus Room (`timer.html`)
* **Custom Pomodoro Engine:** JS `setInterval` countdown timer with customizable focus/break durations and audio alarms.
* **Ambient Audio Stream:** Embedded YouTube iframe for Lofi/Study music.
* **Integrated Task Manager:** Priority tagging (P1/P2/P3), active task pinning, live progress bar calculations, and state-filtered tabs (All/Pending/Completed).

### 3. Analytics (`stats.html`)
* **Telemetry Sync:** Reads across multiple `localStorage` keys to aggregate total active focus hours and total completed tasks.
* **Timestamped Audit Log:** A persistent history panel that logs every checked-off task with its priority badge, parent study block, and exact completion timestamp.

---

## 📂 File Structure

```text
kairo-workspace/
├── index.html     # Page 1: Dashboard & Block Setup
├── timer.html     # Page 2: Pomodoro Timer & Tasks
├── stats.html     # Page 3: Telemetry & Audit Log
└── README.md      # Project documentation
```

---

## 🛠️ How to Evaluate (For Instructors)

To fully test the dynamic capabilities of this application:
1. Open the **Live Demo link** (no installation required).
2. On the **Dashboard**, use the form to add a custom study block. Note the summary metrics updating instantly.
3. Click **Open Focus Room** on your new block. Notice how the URL passes the block name, and the page context updates dynamically.
4. Add a task, start the timer, and check the task off. 
5. Navigate to the **Analytics** tab to view the timestamped completion log and updated focus hours proving cross-page data persistence.
6. Toggle **Dark Mode** on any page; note how the preference persists as you navigate across the app. 
