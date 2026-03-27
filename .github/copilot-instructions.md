# Copilot Instructions

## Project Overview

This is a TypeScript practice project with a minimal structure focused on learning and experimentation. The codebase consists of:
- `main.ts` - Primary entry point containing example console output and user information
- `src/page.ts` - Additional module with similar console output patterns
- Configuration files and sensitive data management

## Architecture & Structure

**TypeScript as Primary Language**: The project uses TypeScript exclusively. All code should follow TypeScript conventions and include type annotations where applicable.

**Entry Point**: `main.ts` serves as the main module. References between modules should be imported from here or via `src/` directory modules.

**Minimal Dependencies**: This is a learning project without external frameworks or complex dependencies. Focus on vanilla TypeScript patterns.

## Critical Conventions

### Sensitive Data Handling
- **Credential Files**: `passwords.txt` and `secret.txt` are intentionally gitignored (see `.gitignore`)
- **Never commit sensitive information**: These files should never be tracked in git. Use environment variables or secure vaults for production credentials
- **File patterns to exclude**: Any file containing secrets, tokens, or credentials should be added to `.gitignore` immediately

### Code Patterns
- **Console logging**: Both `main.ts` and `src/page.ts` use `console.log()` for output (e.g., `console.log("scenario2")`)
- **Type annotations**: Use TypeScript's type system (example: `const userName: string = "Kivers"`)
- **No complex state management**: This project doesn't use frameworks, so keep state simple and local to modules

## Developer Workflows

### Building & Running
- Run TypeScript files using Node.js with `ts-node` or compile with `tsc` first
- No build configuration exists yet; add `tsconfig.json` if TypeScript compilation options are needed

### Testing
- No test framework is configured; add testing setup if needed

### Git Best Practices
- Always verify `.gitignore` includes sensitive files before committing
- Check for credential leaks with `git status` before pushing

## Key Integration Points

**Module Structure**: Keep `src/` for organized module grouping. Import from `src/` submodules into `main.ts` as needed.

**No External APIs/Services**: Currently, no external integrations exist. If adding APIs, document configuration requirements clearly.

## Common Tasks

- **Adding a new module**: Create files in `src/`, export types/functions, import in `main.ts`
- **Adding dependencies**: Update package.json (if created) and document in this file
- **Managing credentials**: Use `.gitignore` + document expected environment variables in a `docs/` folder, never commit actual secrets
