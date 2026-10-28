---
title: 'npm TypeScript Package Template'
layout: 'page'
description: 'A template project for creating a TypeScript package for npm.'
---

## About This Project

A template project for creating a TypeScript package for npm.

## New Package Steps

Follow these steps after creating a new repository from this template.
The same steps appear in `README.md`, `docs/index.md`, and `.github/copilot-instructions.md`; keep all three copies identical until the final step removes them.

1. In `package.json`, update `name`, `version`, `description`, `author`, `homepage`, `repository.url`, `bugs.url`, and `keywords` for the new package and repository.
2. In `.github/workflows/package-publish.yml`, change the `scope` of the GitHub Packages job (`@blwatkins`) to the GitHub account or organization that owns the new repository. GitHub Packages requires the package name's scope to match that owner. If the npm scope of the new package does not match it, remove the `publish-github` job instead, rename the workflow to drop "GitHub Package" from its `name`, and remove GitHub Packages from the "Tech Stack" section and from the name and description of the `package-publish.yml` row of the "GitHub Actions CI" table in `.github/copilot-instructions.md`.
3. In `tsdown.config.ts`, rename `globalName` for the new package. It only applies to IIFE or UMD output, so remove it and `outputOptions.globals` if the package will only ever ship ESM.
4. Replace the `hello-world` example module:
   - Replace `src/hello-world/` and `test/hello-world/` with the package's own modules, and re-export each module from `src/index.ts`.
   - Point the `entryPoints` in `typedoc.json` at each module's index file.
   - Update the "Directory Structure" section of `.github/copilot-instructions.md`.
5. In `typedoc.json`, update `navigationLinks` and `customFooterHtml`.
6. In `docs/_config.yml`, update `title`, `description`, and `minima.social_links`. Leave the npm social link `url` as `'#'` until the first publish.
7. In `README.md` and `docs/index.md`, update the title, description, documentation links, and every badge and link that names `@blwatkins/template` or `npm-typescript-package-template`.
8. Remove the sample documentation:
   - Delete the contents of `docs/doc/` and `docs/releases/`.
   - Remove the sample entries from `docs/releases.md`, and update its front matter `author` and `description`.
   - Replace the content of `docs/resources-and-references.md`, and update its front matter `author` and `description`.
9. Update the owners in `.github/CODEOWNERS` and the accounts in `.github/FUNDING.yml`, or remove `FUNDING.yml`.
10. Update the copyright holder and year in `LICENSE`, every file header, `velocity-copyright-template.txt`, the footer of `README.md`, and `docs/_includes/footer.html`.
11. Review `.github/copilot-instructions.md`:
    - Update the "Project Overview" section.
    - Decide whether to keep the shared error type, assertion, and type guard conventions. To keep them, add `@blwatkins/utils` as a dependency. To drop them, remove the sections that reference `@blwatkins/utils`.
12. Run `npm install` to regenerate `package-lock.json` for the new package name, then run `npm run validate`.
13. Remove this "New Package Steps" section from `README.md`, `docs/index.md`, and `.github/copilot-instructions.md`.

## Documentation

- [Sample Documentation](./doc/index.html)
- [Sample Releases](./releases.md)

## License

The source code of this project is licensed under the [MIT License](https://opensource.org/license/mit).
The full text of the license is included with the project source code.

## Project Links and Status Badges

### [npm](https://www.npmjs.com/package/@blwatkins/template)

![npm License](https://badgen.net/npm/license/@blwatkins/template)
![npm Version](https://badgen.net/npm/v/@blwatkins/template)
![npm @alpha Version](https://badgen.net/npm/v/@blwatkins/template/alpha)
![npm Types](https://badgen.net/npm/types/@blwatkins/template)
![npm Node Version](https://badgen.net/npm/node/@blwatkins/template)
![npm Weekly Downloads](https://badgen.net/npm/dw/@blwatkins/template)
![npm Total Downloads](https://badgen.net/npm/dt/@blwatkins/template)
![npm Last Update](https://img.shields.io/npm/last-update/%40blwatkins%2Ftemplate)
![npm Unpacked Size](https://img.shields.io/npm/unpacked-size/%40blwatkins%2Ftemplate)

### [Socket](https://socket.dev/npm/package/@blwatkins/template)

![Socket Score](https://badge.socket.dev/npm/package/@blwatkins/template)

### Bundlephobia

- [Bundlephobia - `@blwatkins/template`](https://bundlephobia.com/package/@blwatkins/template)

### [Package Phobia](https://packagephobia.com/result?p=%40blwatkins%2Ftemplate)

![Package Phobia Install Size](https://badgen.net/packagephobia/install/@blwatkins/template)
![Package Phobia Publish Size](https://badgen.net/packagephobia/publish/@blwatkins/template)

### [GitHub](https://github.com/blwatkins/npm-typescript-package-template)

![GitHub License](https://badgen.net/github/license/blwatkins/npm-typescript-package-template)
![GitHub Dependabot](https://badgen.net/github/dependabot/blwatkins/npm-typescript-package-template)
![GitHub Latest Release](https://badgen.net/github/release/blwatkins/npm-typescript-package-template)
![GitHub Releases](https://badgen.net/github/releases/blwatkins/npm-typescript-package-template)
![GitHub Last Commit](https://badgen.net/github/last-commit/blwatkins/npm-typescript-package-template)
![GitHub Commits](https://badgen.net/github/commits/blwatkins/npm-typescript-package-template)
![GitHub Commit Activity](https://img.shields.io/github/commit-activity/y/blwatkins/npm-typescript-package-template)
![GitHub Code Size in Bytes](https://img.shields.io/github/languages/code-size/blwatkins/npm-typescript-package-template)
![GitHub Repo Size](https://img.shields.io/github/repo-size/blwatkins/npm-typescript-package-template)
![GitHub Repo File or Directory Count](https://img.shields.io/github/directory-file-count/blwatkins/npm-typescript-package-template)
![GitHub Language Count](https://img.shields.io/github/languages/count/blwatkins/npm-typescript-package-template)

### GitHub Actions

![CodeQL](https://github.com/blwatkins/npm-typescript-package-template/actions/workflows/codeql.yml/badge.svg)
![npm Validate](https://github.com/blwatkins/npm-typescript-package-template/actions/workflows/npm-validate.yml/badge.svg)
![Deploy GitHub Pages with Jekyll](https://github.com/blwatkins/npm-typescript-package-template/actions/workflows/gh-pages-jekyll.yml/badge.svg)

## Sources and Technical Notes

- [Resources and References](./resources-and-references.md)

## Thank Yous

A huge thank you to all the open source contributors who have made this project possible by creating and maintaining the libraries and tools used in this project, and to the open source community for fostering collaboration and innovation.

A special thank you to all the educators, mentors, and content creators who have shared their knowledge and expertise in the fields of algorithmic art, web development, and computer science.
Thank you for giving me the tools, resources, opportunities, support, and inspiration to learn and grow as a developer.
