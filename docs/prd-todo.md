# Product Requirements Document (PRD) - Todo App Upgrade: Due Dates, Priorities, Filters

## 1. Overview

We are upgrading the basic TODO app (currently title + completed) to support due dates, simple priorities, and basic filters so users can better understand urgency and focus on what matters today. Scope is intentionally lean and client-confirmed for a teachable MVP with no backend changes and local-only storage.

---

## 2. MVP Scope

- Data model & validation
  - title: required
  - priority: "P1" | "P2" | "P3"; default "P3" when not provided
  - dueDate: optional ISO `YYYY-MM-DD`; invalid values are ignored (treated as absent)
- User functionality
  - Create/edit tasks with title, priority, and optional due date
  - Filter tabs: All, Today, Overdue
  - Filter behavior: Today/Overdue show incomplete tasks only; All includes completed tasks
- UI behavior
  - Display priority with simple color-coded badges: P1 (red), P2 (orange), P3 (gray)
- Storage & architecture
  - Local storage only; no backend or external storage; no backend changes

---

## 3. Post-MVP Scope

- Overdue highlighting: visually emphasize overdue tasks in the list (e.g., red styling)
- Sorting rules:
  - Order: overdue first → priority (P1→P3) → due date ascending → undated last

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user functionality
- Keyboard navigation / advanced accessibility features
- External storage or backend changes (stays local-only)
