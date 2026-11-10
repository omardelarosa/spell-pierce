# Spell Pierce

This is a static site for my music build using Astro.

## Astro Commands

All commands are run from the root of the project, from a terminal:

| Command              | Action                                           |
| :------------------- | :----------------------------------------------- |
| `pnpm install`       | Installs dependencies                            |
| `pnpm dev`           | Starts local dev server at `localhost:4321`      |
| `pnpm build`         | Build your production site to `./dist/`          |
| `pnpm preview`       | Preview your build locally, before deploying     |
| `pnpm astro ...`     | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro --help`  | Get help using the Astro CLI                     |

## Developing Locally

| Prerequisites                                                                         |
| :------------------------------------------------------------------------------------ |
| [Node.js](https://nodejs.org/) 24 LTS (pinned in `.nvmrc` — run `nvm use`).           |
| [pnpm](https://pnpm.io/installation) — the exact version is pinned in `package.json`. |

1. Run `nvm use`, then `pnpm install` in the project root.
2. Run `pnpm dev` and visit [localhost:4321](http://localhost:4321).

## Dependency security

`pnpm-workspace.yaml` hardens installs:

- **`minimumReleaseAge`**: versions published less than 7 days ago are not installed.
- **`trustPolicy: no-downgrade`**: installs fail if a version has weaker publish provenance than earlier releases. Hand-reviewed false positives are listed by exact version in `trustPolicyExclude`, with a note on why.
- **`allowBuilds`**: dependency install scripts only run for packages listed here.
- **`blockExoticSubdeps`**: transitive dependencies must come from the npm registry.

If an install fails on one of these checks, review the package before adding an exception.
