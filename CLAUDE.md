# CLAUDE.md - AI Assistant Guide for git_tutorial Repository

## Repository Overview

This is a **Git Tutorial Repository** designed to demonstrate various Git workflows and operations. The repository uses simple HTML files to illustrate Git concepts including branching, merging, conflict resolution, pull requests, and GitHub Flow.

**Repository**: hify24rer/git_tutorial
**Primary Language**: Japanese (日本語)
**Project Type**: Educational/Tutorial
**Tech Stack**: Static HTML files

---

## Repository Structure

```
git_tutorial/
├── .git/                  # Git repository metadata
├── .gitignore            # Git ignore rules (secret.txt, .DS_Store)
├── index.html            # Main tutorial page with Git concepts
├── home.html             # Home page (demonstrates git pull)
├── master.html           # Master branch demonstration file
├── master2.html          # Additional master branch file
├── feature.html          # Feature branch demonstration
├── feature2.html         # Additional feature branch file
├── first.html            # Empty file (for tutorial purposes)
├── second.html           # Empty file (for tutorial purposes)
└── third.html            # Empty file (for tutorial purposes)
```

### File Descriptions

- **index.html**: Core tutorial file containing Git command references:
  - `git status`
  - `git diff`
  - `git commit --amend`
  - `git merge`
  - コンフリクト (Conflict resolution)
  - pull request
  - GitHub Flow

- **Feature Files**: Demonstrate branch-based development
- **Empty HTML Files** (first.html, second.html, third.html): Used to demonstrate file addition and tracking

---

## Git Workflow & History

### Branch Strategy

The repository demonstrates multiple Git workflows:

1. **Feature Branch Workflow**: Creating feature branches, making changes, and merging
2. **Pull Request Workflow**: Using PRs for code review and integration
3. **GitHub Flow**: Lightweight branch-based workflow
4. **Conflict Resolution**: Demonstrates handling merge conflicts

### Current Branch

- Working on: `claude/claude-md-mi2n18uvykrjtxg2-01FnZRutRMAYGdeK2RnrJc2L`
- Branch naming convention for AI assistants: `claude/claude-{descriptive-name}-{session-id}`

### Key Commits (Chronological Order)

```
b560ec5 - .gitignoreファイルを追加
6192936 - git commit --amendを追記
d36f079 - Create home.html
20e2771 - Update home.html
0b14c08 - master.htmlファイルを新規作成
2a4b6e5 - git mergeを追記
f66ba86 - feature.htmlファイルを新規追加
4cde725 - featureを追記
4b0182e - コンフリクトを追記
710d8b4 - conflictを追記
1b477ea - Merge branch 'feature'
89ff13e - pull requestを追記
340d121 - Merge pull request #1 from hify24rer/pull_request
ebb2326 - GitHub Flowを追記
208a528 - Merge pull request #2 from hify24rer/github_flow
191ca43 - master2を新規作成
a011d42 - feature2を新規作成
e2408d3 - first.htmlとsecond.htmlを追加
2882633 - third.htmlを追加
```

---

## Development Conventions

### 1. Commit Messages

**Language**: Japanese (日本語)
**Format**: Descriptive action + object

**Examples**:
- ✅ `{filename}ファイルを新規作成` - Create new file
- ✅ `{feature}を追記` - Add feature
- ✅ `{filename}を追加` - Add file
- ✅ `Merge pull request #{number} from {branch}` - PR merges

**Pattern**:
- Use Japanese for all commit messages
- Follow the format: `[action][object]`
- Be concise and descriptive

### 2. File Naming

- Lowercase filenames (e.g., `index.html`, `feature.html`)
- Descriptive names that indicate purpose
- Sequential numbering for related files (e.g., `master2.html`, `feature2.html`)

### 3. Branch Naming

**Convention**:
- Feature branches: `feature`, `pull_request`, `github_flow`
- AI assistant branches: `claude/claude-{description}-{session-id}`
- Descriptive, lowercase, use underscores for spaces

### 4. Ignored Files

Per `.gitignore`:
```
secret.txt
.DS_Store
```

**Never commit**:
- Secret or sensitive files
- OS-specific files (.DS_Store for macOS)
- Build artifacts or temporary files

---

## Working with This Repository

### For AI Assistants

#### Git Operations

**Branch Management**:
```bash
# Always work on designated claude/ branch
git checkout claude/claude-md-{description}-{session-id}

# Create branch if it doesn't exist
git checkout -b claude/claude-md-{description}-{session-id}
```

**Committing Changes**:
```bash
# Stage changes
git add <files>

# Commit with Japanese message
git commit -m "$(cat <<'EOF'
[Japanese commit message here]
EOF
)"

# Push to remote with upstream tracking
git push -u origin claude/claude-md-{description}-{session-id}
```

**Critical Requirements**:
- Branch MUST start with `claude/` and end with matching session ID
- Push will fail with 403 if branch naming convention is not followed
- Use exponential backoff (2s, 4s, 8s, 16s) for network retry operations
- Maximum 4 retry attempts for push/fetch/pull operations

#### Content Guidelines

1. **Language**: Maintain Japanese for user-facing content
2. **HTML Format**: Keep simple HTML structure (minimal markup)
3. **Tutorial Purpose**: Preserve educational nature of files
4. **Consistency**: Match existing file patterns and styles

#### Making Changes

When modifying files:
1. Read existing files first to understand structure
2. Maintain consistent HTML format
3. Use Japanese text for content
4. Keep files simple and focused
5. Test changes don't break tutorial flow

#### Creating New Files

If adding new HTML files:
1. Use lowercase filenames
2. Keep content minimal and tutorial-focused
3. Follow existing file patterns
4. Add descriptive Japanese content
5. Update this CLAUDE.md if structure changes

---

## Common Tasks

### Adding a New Tutorial Concept

1. Identify the concept to add
2. Determine if it fits in `index.html` or needs a new file
3. Add Japanese description of the Git command/concept
4. Commit with format: `{concept}を追記`
5. Push to appropriate branch

### Demonstrating a Merge Conflict

1. Create changes on different branches affecting the same lines
2. Attempt merge to create conflict
3. Resolve conflict appropriately
4. Commit with message describing resolution

### Creating a Pull Request

1. Make changes on feature branch
2. Push branch to remote
3. Create PR with descriptive title (Japanese preferred)
4. Include clear description of changes
5. Reference related tutorial concepts

---

## Repository State

**Current Status**: Clean working directory
**Latest Commit**: `2882633 - third.htmlを追加`
**Active Branch**: `claude/claude-md-mi2n18uvykrjtxg2-01FnZRutRMAYGdeK2RnrJc2L`

### File Status Summary

All tracked files are committed. No pending changes.

**Total Files**: 9 HTML files + 1 .gitignore
**Empty Files**: first.html, second.html, third.html (intentionally empty for tutorial)

---

## Best Practices for AI Assistants

### DO ✅

- Write commit messages in Japanese matching existing patterns
- Maintain simple HTML structure
- Follow branch naming conventions strictly
- Preserve educational purpose of repository
- Read files before modifying them
- Keep changes minimal and focused
- Test Git operations work as expected
- Document significant structural changes in this file

### DON'T ❌

- Push to wrong branch names (will fail with 403)
- Use English for commit messages (unless specifically requested)
- Over-complicate HTML structure
- Add unnecessary dependencies or frameworks
- Commit sensitive information
- Break existing tutorial flows
- Skip reading files before editing
- Create complex nested structures

---

## Troubleshooting

### Push Fails with 403

**Cause**: Branch name doesn't match required pattern
**Solution**: Ensure branch starts with `claude/` and ends with correct session ID

### Merge Conflicts

**Approach**:
1. Identify conflicting sections
2. Understand intent of both changes
3. Resolve maintaining tutorial clarity
4. Test merged content makes sense
5. Commit resolution with descriptive message

### Network Errors

**Strategy**:
- Retry up to 4 times
- Use exponential backoff: 2s, 4s, 8s, 16s
- Log failures for debugging
- Report persistent issues to user

---

## Contact & Contribution

**Repository Owner**: hify24rer
**Purpose**: Git workflow education and demonstration
**Contribution Style**: Pull requests with clear Japanese descriptions

---

## Version History

- **2025-11-17**: Initial CLAUDE.md creation - comprehensive repository documentation for AI assistants
- **Latest Commit**: 2882633 - third.htmlを追加

---

## Quick Reference

### Git Commands Demonstrated in This Repo

| Command | File Reference | Purpose |
|---------|---------------|---------|
| `git status` | index.html:2 | Check repository status |
| `git diff` | index.html:3 | View changes |
| `git commit --amend` | index.html:4 | Modify last commit |
| `git merge` | index.html:5 | Merge branches |
| `git pull` | home.html:2 | Fetch and merge changes |

### Common File Operations

```bash
# View repository structure
ls -la

# Check git status
git status

# View git history
git log --oneline --graph --all --decorate

# View branches
git branch -a
```

---

**Document Maintained By**: AI Assistants working with this repository
**Last Updated**: 2025-11-17
**Document Version**: 1.0
