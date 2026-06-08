# Motivational Interviewing Skill

A Claude Code / OpenCode / Codex / pi skill that teaches AI agents to practice motivational interviewing — an evidence-based approach for helping people work through ambivalence, stuckness, and difficult decisions.

## What it does

When invoked, the agent shifts into MI mode: reflecting what you say, asking open questions, exploring both sides of your ambivalence, and never telling you what to do. It helps you hear yourself think.

## Installation

### Claude Code

```bash
/plugin marketplace add https://github.com/heartpunk/motivational-interviewing-skill.git
/plugin install motivational-interviewing@motivational-interviewing-skill
```

Then invoke with `/motivational-interviewing`.

### OpenCode

OpenCode natively supports SKILL.md and auto-loads from Claude Code skill directories. If you installed via Claude Code above, OpenCode picks it up automatically. Otherwise:

```bash
# Project-level
mkdir -p .opencode/skills/motivational-interviewing
cp motivational-interviewing/skills/motivational-interviewing/SKILL.md \
   .opencode/skills/motivational-interviewing/SKILL.md

# Global
mkdir -p ~/.config/opencode/skills/motivational-interviewing
cp motivational-interviewing/skills/motivational-interviewing/SKILL.md \
   ~/.config/opencode/skills/motivational-interviewing/SKILL.md
```

Or register in `opencode.json`:

```json
{
  "skills": {
    "paths": ["path/to/motivational-interviewing-skill/motivational-interviewing/skills"]
  }
}
```

### Codex

Add the marketplace in settings, then install the plugin.

### Pi

Add the skills directory to your pi settings:

```json
{
  "skills": ["path/to/motivational-interviewing-skill/motivational-interviewing/skills"]
}
```

## How it works

The skill is trained on patterns from the [AnnoMI dataset](https://github.com/uccollab/AnnoMI) — 133 expert-annotated motivational interviewing conversations. High-quality transcripts provide the core techniques (reflective listening, open questions, scaling, decisional balance, autonomy emphasis). Low-quality transcripts provide the "never do this" list (giving unsolicited advice, arguing with the client, minimizing concerns, jumping to solutions).

## When to use it

- You're stuck between options and don't know which way to go
- You feel ambivalent about starting, stopping, or changing something
- You keep going in circles and want help breaking out
- You want someone to help you think without telling you what to think

## License

CC-BY-4.0. See LICENSE.txt.

## References

- Miller, W. R., & Rollnick, S. (2013). *Motivational Interviewing: Helping People Change* (3rd ed.). Guilford Press.
- Wu, Z., Balloccu, S., Kumar, V., Helaoui, R., Reiter, E., Reforgiato Recupero, D., & Riboni, D. (2022). Anno-MI: A Dataset of Expert-Annotated Counselling Dialogues. *ICASSP 2022*.
