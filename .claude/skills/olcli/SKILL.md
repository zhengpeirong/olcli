```markdown
# olcli Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `olcli` TypeScript codebase. It covers file naming, import/export styles, commit message habits, and testing patterns, providing a practical guide for contributing to or maintaining the repository.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myUtilityFile.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // utils.ts
    export function myFunction() { ... }
    ```

### Commit Messages
- Freeform style, sometimes with prefixes.
- Average length: ~34 characters.
  - Example: `fix: handle edge case in parser`

## Workflows

### Adding a New Module
**Trigger:** When you need to add new functionality.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Write your TypeScript code, using named exports.
3. Import your module using a relative path where needed.
4. Add corresponding test files with the `.test.ts` suffix.
5. Commit your changes with a clear, concise message.

### Running Tests
**Trigger:** When you want to verify code correctness.
**Command:** `/run-tests`

1. Identify test files (pattern: `*.test.*`).
2. Use the project's test runner (framework unknown; check project scripts or documentation).
3. Run the tests and review results.

### Refactoring Code
**Trigger:** When improving or restructuring existing code.
**Command:** `/refactor`

1. Update file names to camelCase if necessary.
2. Ensure all imports/exports use the relative and named conventions.
3. Update or add tests as needed.
4. Commit with a descriptive message.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `utils.test.ts`).
- The specific testing framework is not detected; check for scripts or documentation for details.
- Place tests alongside or near the files they cover.

  Example:
  ```
  src/
    utils.ts
    utils.test.ts
  ```

## Commands
| Command      | Purpose                                   |
|--------------|-------------------------------------------|
| /add-module  | Scaffold and add a new module             |
| /run-tests   | Run all test files in the codebase        |
| /refactor    | Refactor code to follow project patterns  |
```