# Contributing to QyverixAI

Thank you for your interest in contributing! This project is designed to be beginner-friendly. Please read the guidelines below to get started.

## How to Contribute

1. **Fork the repository** and clone it locally.
   ```bash
   git clone https://github.com/YOUR_USERNAME/AI-dev-assistant.git
   cd AI-dev-assistant
   ```

2. **Create a new branch** for your feature or bugfix.
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes** in the appropriate folder (`backend/` or `frontend/`).

4. **Test your changes** before submitting.
   ```bash
   cd backend
   pytest -q
   ```

5. **Commit with clear messages** (see Commit Message Conventions below).

6. **Submit a pull request** with a clear description of your changes.

---

## Commit Message Conventions

Follow this format for commit messages:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Examples:**
- `fix(debug): add Python AST checks for syntax errors`
- `feat(frontend): add engine status badge`
- `docs(readme): add local setup instructions`
- `style(css): improve engine badge styling`

**Types:**
- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation
- `style` - Code style (no functional change)
- `refactor` - Code restructuring
- `test` - Test additions or fixes
- `chore` - Dependencies, build setup

---

## Pull Request Format

**PR Title:** Use the commit convention above.

**PR Description (required):**
```markdown
## What does this PR do?
[Brief description of changes]

## Why are these changes needed?
[Motivation and context]

## How was this tested?
[Testing approach or steps to verify]

## Screenshots (if applicable)
[Add screenshots for UI changes]

## Related Issues
Closes #123
```

**All PRs must:**
- Pass all CI/CD checks (tests, linting)
- Include a descriptive title and body
- Reference any related issues
- Not modify `LICENSE` or other critical files without discussion

---

## Code Style

### Python (Backend)
- Follow [PEP 8](https://pep8.org/) style guide.
- Use clear variable names: `user_age` instead of `ua`.
- Write docstrings for all functions:
  ```python
  def analyze_code(code: str) -> dict:
      """Analyze code and return explanation, bugs, and improvements.
      
      Args:
          code: Source code string
          
      Returns:
          dict with keys 'explanation', 'debugging', 'suggestions'
      """
  ```
- Keep functions focused and under 50 lines.
- Use type hints where applicable.

### JavaScript (Frontend)
- Use beginner-friendly variable names.
- Add comments for complex logic.
- Keep functions small and focused.
- Use `const` and `let` (avoid `var`).

### General
- Write comments explaining the **why**, not the **what**.
- Keep lines under 100 characters.
- Use meaningful commit messages.

---

## Testing

### Backend
```bash
cd backend
pytest -q                   # Run all tests
pytest -q -k test_name     # Run specific test
```

**All new features must include tests.**

### Frontend
Manual testing in browser is acceptable for UI changes.

---

## Review Timeline

- **Typical review time:** 24–48 hours
- **Merging after approval:** Within 24 hours of final approval
- **Reviewers will ask for changes** if needed - don't be discouraged!

---

## Issues

- If you find a bug or want a new feature, open an [issue](https://github.com/imDarshanGK/AI-dev-assistant/issues/new) with details.
- Look for issues labeled [good first issue](https://github.com/imDarshanGK/AI-dev-assistant/labels/good%20first%20issue) if you're new.

---

## Community & Support

**Questions?** Ask in [GitHub Discussions](https://github.com/imDarshanGK/AI-dev-assistant/discussions).

**Found a bug?** Open an [issue](https://github.com/imDarshanGK/AI-dev-assistant/issues/new).

---

## Example API Request

```bash
curl -X POST "http://localhost:8000/explanation/" \
  -H "Content-Type: application/json" \
  -d '{"code": "print(1)"}'
```

---

## Local Setup (Quick Reference)

```bash
git clone https://github.com/imDarshanGK/AI-dev-assistant.git
cd AI-dev-assistant/backend
pip install -r requirements.txt
uvicorn app.main:app --reload
# Open http://localhost:8000/app/ in browser
```

---

Thank you for contributing! 🎉
