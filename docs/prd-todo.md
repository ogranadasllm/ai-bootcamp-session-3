# Product Requirements Document (PRD) - TODO App Enhancement: Due Dates, Priorities & Filters

## 1. Overview

We are upgrading the basic TODO app to support due dates, priority levels, and filtering capabilities. Currently, the app only tracks task titles and completion status. This enhancement will enable users to better organize and prioritize their tasks by setting deadlines, assigning priority levels, and quickly filtering tasks based on urgency and timeframes. The goal is to make the app more practical and useful for daily task management without adding unnecessary complexity.

---

## 2. MVP Scope

### Core Features

**Due Dates**
- Add an optional due date field to each task
- Users can set, edit, or leave the due date blank
- Display due dates clearly alongside each task
- Visually highlight overdue tasks in red to make them stand out
- Calculate overdue status by comparing due date with current date

**Priority Levels**
- Support three priority levels: P1 (High), P2 (Medium), P3 (Low)
- Display priorities as color-coded badges:
  - P1: Red badge
  - P2: Orange badge
  - P3: Gray badge
- Allow users to assign or change priority when creating or editing tasks

**Filtering & Views**
- Implement three filter tabs for quick view switching:
  - **All**: Show all tasks (including completed)
  - **Today**: Show only incomplete tasks due today
  - **Overdue**: Show only incomplete tasks that are past their due date
- Completed tasks should only appear in the "All" view
- Active filter tab should be visually indicated

**Sorting Logic**
- Apply consistent sorting across all views:
  1. Overdue tasks first
  2. Then sort by priority (P1, then P2, then P3)
  3. Then sort by due date (earliest first)
  4. Tasks without due dates appear last
- Maintain this sorting order regardless of active filter

**UI/UX Requirements**
- Keep the interface simple and intuitive
- Use color consistently for visual cues (red for overdue/P1, orange for P2, gray for P3)
- Maintain the current simple design aesthetic
- Continue using local storage for data persistence

---

## 3. Post-MVP Scope

**Notifications & Reminders**
- Push notifications or email reminders for upcoming or overdue tasks
- Configurable reminder settings (e.g., 1 hour before, 1 day before)

**Recurring Tasks**
- Ability to create tasks that repeat on a schedule (daily, weekly, monthly)
- Automatic recreation of recurring tasks upon completion

**Advanced Filtering**
- Additional filters such as "This Week", "Next Week", "By Priority"
- Custom date range filters
- Search functionality for task titles

**Enhanced Accessibility**
- Full keyboard navigation support
- Screen reader optimization
- High contrast mode
- Customizable color schemes for color-blind users

**Collaboration Features**
- Task sharing with other users
- Comments and notes on tasks
- Task assignment to team members

---

## 4. Out of Scope

**For MVP and Post-MVP:**
- Keyboard navigation and special accessibility features (keeping it simple for now)
- Push notifications or email alerts
- Recurring task functionality
- Task categories or tags
- Task dependencies or subtasks
- Time tracking or time estimates
- Calendar integration
- Mobile native applications
- Multi-user collaboration
- Cloud synchronization or backend services (continuing with local storage)
- Task attachments (files, images, links)
- Task descriptions beyond the title
- Bulk operations (multi-select, bulk edit, bulk delete)
