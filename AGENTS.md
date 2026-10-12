# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a minimal workspace. As code is added, keep the layout predictable and shallow:

- `src/` for application source code and reusable modules.
- `tests/` for automated tests that mirror the structure of `src/`.
- `assets/` for static files such as images, fixtures, or sample data.
- `docs/` for design notes, API references, and contributor documentation.

Prefer small, focused modules. Avoid placing generated files, build outputs, or local editor settings in source directories.

## Build, Test, and Development Commands

No project-specific build system is configured yet. When adding tooling, document commands here and keep them runnable from the repository root. Common examples include:

- `npm install` to install JavaScript dependencies.
- `npm test` to run the test suite.
- `npm run build` to create a production build.
- `npm run dev` to start a local development server.

If another stack is introduced, use its standard entry points, such as `make test`, `pytest`, `cargo test`, or `dotnet test`.

## Coding Style & Naming Conventions

Match the conventions of the language and framework introduced in the repository. Use consistent indentation, descriptive names, and small functions with clear responsibilities. Suggested defaults:

- Use `camelCase` for JavaScript/TypeScript variables and functions.
- Use `PascalCase` for classes, components, and exported types.
- Use `kebab-case` or `snake_case` for filenames, following the dominant ecosystem convention.

Add formatter and linter commands when tooling is selected, and run them before opening a pull request.

## Testing Guidelines

Place tests in `tests/` or beside source files using a clear suffix such as `.test.*` or `.spec.*`. Tests should cover normal behavior, edge cases, and regression fixes. Keep fixtures small and store shared test data under `tests/fixtures/` when needed.

## Commit & Pull Request Guidelines

There is no established Git history yet. Use concise, imperative commit messages, for example `Add user settings model` or `Fix validation error handling`. Pull requests should include a short summary, testing performed, related issues, and screenshots or logs for user-visible changes.

## Security & Configuration Tips

Do not commit secrets, credentials, or machine-specific configuration. Store local values in ignored environment files such as `.env.local`, and document required variables in `.env.example` when configuration is introduced.
