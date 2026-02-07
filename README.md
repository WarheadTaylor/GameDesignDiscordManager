# GameDesignDiscordManager

A Discord bot that manages a dedicated game design category — providing read-only forums for design topics, discussion channels for feedback and intake, and AI-powered tools to structure participant input into organized, living design documents.

## Overview

Game design discussions often happen across scattered messages, making it hard to track decisions and evolving ideas. This bot solves that by creating a structured workflow within Discord:

1. **Participants submit feedback** through discussion channels or structured intake commands
2. **AI processes and organizes** that feedback — categorizing, summarizing, and formatting it
3. **Read-only forum posts are created or updated** so the team always has a clean, current view of each design topic

## Channel Structure

### Read-Only Forums

A forums section containing topics covering areas of game design, including:

- Mechanics
- Narrative / Lore
- Level Design
- Economy / Balancing
- UI / UX
- Art Direction

Topics can also be created dynamically as the project evolves. Forum posts serve as living documents that are updated over time as feedback is incorporated.

### Discussion & Intake Channels

Text channels where team members can:

- Submit raw ideas and feedback
- Have open-ended design discussions
- Provide structured input via slash commands or modal forms

## Key Features

### Structured Intake via Slash Commands & Modals

The bot provides Discord slash commands and modal forms for collecting structured feedback (e.g., `/submit-feedback topic:"Combat" feedback:"The dodge feels too slow"`). This ensures AI processing is reliable and feedback is routed to the correct design topic.

### Threaded Discussion Summaries

The bot monitors discussion channels and can generate AI-powered summaries when:

- A thread reaches a configurable length
- A moderator reacts with a designated emoji
- A moderator triggers a summary command

Summaries are posted or appended to the relevant read-only forum topic, keeping forums up to date.

### Topic Versioning & Changelog

Since forum posts are updated over time by AI, the bot maintains a version history or changelog within each post. This lets the team see how a design area has evolved based on accumulated feedback.

### Feedback Sentiment & Priority Tagging

Incoming feedback is categorized by the AI with:

- **Sentiment** — positive, concern, or suggestion
- **Priority** — high, medium, low

A digest is presented to moderators before any forum updates are applied, ensuring a human-in-the-loop review step.

## Permissions Model

- **Participants** — Can submit feedback and discuss in text channels
- **Moderators** — Can trigger summaries, approve AI-generated forum updates, and manage topics
- **Forums** — Read-only for all participants; only the bot writes to them