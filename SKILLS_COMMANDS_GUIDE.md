# cdecli Skills Commands Guide

This guide covers the core commands to create, inspect, update, and manage skills with `cdecli`.

## 1) List skills

```bash
cdecli skills list
```

Shows available remote skills and local/global installed skills.

## 2) Create a new skill scaffold

```bash
cdecli skills new <skill-name> \
  --template workflow \
  --description "One-line description" \
  --author "<author>" \
  --tag <tag1> --tag <tag2> \
  --force
```

Example:

```bash
cdecli skills new cdecli-workflow-expert \
  --template workflow \
  --description "Expert at creating cdecli workflows" \
  --author "nsharc" \
  --tag cdecli --tag workflow \
  --force
```

Default location:

- `~/.cdecli/skills/<skill-name>/SKILL.md`

## 3) View a skill

```bash
cdecli skills show <skill-name>
```

Example:

```bash
cdecli skills show cdecli-workflow-expert
```

## 4) Update a skill

There is no separate `skills update` subcommand in this CLI version.  
Update by editing the file directly:

- `~/.cdecli/skills/<skill-name>/SKILL.md`

Then re-check:

```bash
cdecli skills show <skill-name>
```

## 5) Install / remove skills

Install:

```bash
cdecli skills install <skill-name>
```

Remove:

```bash
cdecli skills remove <skill-name>
```

## 6) Publish skill (optional)

```bash
cdecli skills publish <skill-name>
```

Quick publish:

```bash
cdecli skills quick-publish <skill-name>
```

## 7) Useful help commands

```bash
cdecli skills --help
cdecli skills new --help
cdecli skills show --help
```
