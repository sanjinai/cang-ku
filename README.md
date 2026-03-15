# PRD for Vibe Coding

A Claude Code skill that helps AI Product Managers quickly write PRDs for rapid prototyping with vibe coding tools.

## What This Skill Does

Transforms vague product ideas into structured, AI-friendly PRDs through a guided conversation. It walks you through:

- Clarifying target users and problems
- Defining core features (3-5 max)
- Setting explicit non-goals to prevent scope creep
- Choosing pragmatic tech stacks
- Establishing measurable success criteria

## When to Use This Skill

Use this skill when you:
- Want to build a prototype with Claude Code, Cursor, or similar AI coding tools
- Have a product idea but need to structure it for AI execution
- Need to write a quick PRD without the overhead of a full business document
- Want to avoid scope creep by thinking through non-goals upfront

## How to Use

Simply tell Claude what you want to build:

```
"I want to make a tool to organize my meeting notes"
```

Or invoke it explicitly:

```
/prd-for-vibe-coding
```

The skill will guide you through a conversational process to clarify your idea and generate a one-page PRD.

## Example Output

The skill generates a structured PRD like this:

```markdown
# Meeting Notes Organizer

## One-Liner
A simple desktop app for solo founders to centralize and search meeting notes.

## Target User & Problem
**Who:** Solo founders who take 5+ meetings per day
**Problem:** Notes scattered across Notion, Apple Notes, and text files - impossible to find anything
**Current State:** Manually searching through 3 different apps
**Desired State:** One searchable repository with project-based organization

## Core Features
1. **Single input interface** - One place to dump all meeting notes
2. **Project tagging** - Tag notes by project and date automatically
3. **Fast search** - Fuzzy search across all notes
4. **Markdown export** - Export individual notes or projects to .md files

## Explicit Non-Goals
- No team sharing or collaboration features
- No mobile app (desktop only)
- No Notion/Slack integrations
- No real-time sync across devices
- No rich text editor (plain text is fine)

## Tech Stack
- **Frontend:** Next.js - Fast to build, good for desktop web apps
- **Backend:** Node.js with local file system - No server needed
- **Database:** SQLite - Perfect for single-user local storage
- **Styling:** Tailwind CSS - Rapid UI development

## Success Criteria
- [ ] Can find any note in under 5 seconds using search
- [ ] All notes from the past 6 months are imported and tagged
- [ ] Can export a project's notes to markdown in one click

## Notes for AI Implementation
- Start with the input interface and SQLite setup first
- Use simple full-text search (no need for Elasticsearch)
- Keep UI minimal - focus on speed over aesthetics
```

## What Makes This Different

This PRD is designed for **AI execution**, not stakeholder approval:

- **Concise:** One page, not 10 pages
- **Specific:** Clear about what NOT to build
- **Actionable:** Every section guides implementation
- **Scoped:** Explicitly prevents feature creep

## File Structure

```
prd-for-vibe-coding/
├── SKILL.md              # Main skill instructions
├── assets/
│   └── prd-template.md   # Reference template with examples
├── evals/
│   └── evals.json        # Test cases
└── README.md             # This file
```

## Tips for Better PRDs

1. **Be specific about users:** "Solo founders who take 5+ meetings/day" beats "busy people"
2. **Frame problems as pain:** "I waste 10 minutes searching" beats "I need better organization"
3. **Non-goals prevent scope creep:** List what you're NOT building
4. **Match tech to skill level:** Suggest simpler stacks for non-technical users
5. **Make success criteria observable:** "Find notes in <5 seconds" beats "fast search"

## Test Cases

The skill includes 5 test scenarios:

1. **Vague idea** - User says "I want to make X" with no details
2. **Specific idea** - User provides context upfront
3. **Overly ambitious** - Scope is too large, needs narrowing
4. **Partial PRD** - User has started, needs completion
5. **Non-technical user** - Needs simpler tech recommendations

Run tests with:
```bash
# Test cases are in evals/evals.json
# Run them manually by copying prompts to Claude Code
```

## Philosophy

This skill embodies a specific philosophy about vibe coding:

- **Speed over perfection:** Ship a working prototype fast
- **Clarity over completeness:** One page beats 10 pages
- **Constraints breed creativity:** Non-goals are as important as goals
- **AI-first documentation:** Write for AI execution, not human approval

## Contributing

Found a bug or have suggestions? This skill is part of your local Claude Code setup. Feel free to modify `SKILL.md` to fit your workflow.

## License

See LICENSE.txt for details.
