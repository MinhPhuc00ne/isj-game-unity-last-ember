# 🤝 Contributing Guidelines

Thank you for your interest in contributing to **Last Ember**!

To ensure code quality, consistency, and a clean project history, all contributors are requested to follow these guidelines.

---

## 1. Branch Naming Conventions

Branch names should clearly indicate their purpose. Use `lowercase` letters, separate words with hyphens (`-`), and follow this format:

`<prefix>/<short-description>`

### Standard Prefixes:

| Prefix | Purpose | Example |
| :--- | :--- | :--- |
| `feature/` | New gameplay features, UI, mechanics | `feature/day-night-cycle`, `feature/monster-ai-pathfinding` |
| `bugfix/` | Bug fixes during development | `bugfix/flashlight-intensity-flicker`, `bugfix/stamina-drain-rate` |
| `hotfix/` | Critical urgent fixes on the main branch | `hotfix/fix-null-pointer-player-interaction` |
| `refactor/` | Code refactoring without changing functionality | `refactor/player-hand-manager`, `refactor/terrain-blend-shader` |
| `docs/` | Documentation updates (README, doc, comments) | `docs/update-contributing-guide`, `docs/add-readme-screenshots` |
| `chore/` | Build scripts, Unity package configs, tool setups | `chore/upgrade-urp-package`, `chore/setup-editor-tools` |

---

## 2. Commit Message Standards (Conventional Commits)

This repository enforces **Conventional Commits**. Every commit message must follow the pattern:

```text
<type>(<scope>): <short summary>

[optional body]

[optional footer]
```

### 2.1. Standard Types

- **`feat`**: A new feature
- **`fix`**: A bug fix
- **`docs`**: Documentation changes
- **`style`**: Formatting changes (white-space, formatting, missing semi-colons, no code change)
- **`refactor`**: A code change that neither fixes a bug nor adds a feature
- **`perf`**: A code change that improves performance
- **`test`**: Adding missing tests or correcting existing tests
- **`chore`**: Changes to the build process or auxiliary tools

### 2.2. Scope (Optional)
Scope specifies the affected module or component in the Unity project.
*Examples:* `player`, `monster`, `environment`, `ui`, `shader`, `audio`, `docs`.

### 2.3. Commit Examples

- `feat(player): add first person flashlight controller`
- `fix(monster): resolve shadow figure pathing visual glitch`
- `refactor(environment): optimize grass wind shader performance`
- `docs(readme): add WIP gameplay screenshots`
- `chore(deps): update TextMesh Pro settings`

---

## 3. Git Workflow & Pull Requests

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MinhPhuc00ne/Last-Ember.git
   ```
2. **Create a new branch:**
   ```bash
   git checkout -b feature/interactive-trunk
   ```
3. **Commit your changes:**
   ```bash
   git add .
   git commit -m "feat(interaction): implement interactable trunk opening animation"
   ```
4. **Push to the remote repository:**
   ```bash
   git push origin feature/interactive-trunk
   ```
5. **Open a Pull Request (PR):**
   - Provide a clear title and description of your changes.
   - List the testing steps performed.
   - Require review from at least 1 team member before merging.

---

## 4. Unity Project Guidelines

- **Meta Files (`.meta`):** Always commit corresponding `.meta` files whenever adding, modifying, or deleting assets in Unity.
- **Scene & Prefab Conflicts:** Avoid concurrent edits on the same Scene or Prefab file. Modularize features into separate Prefabs.
- **Git LFS:** Ensure large binary assets (4K textures, 3D models `.fbx`/`.obj`, audio `.wav`) are tracked via Git LFS.
