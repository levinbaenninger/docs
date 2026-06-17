# Lerndokumentation

This repository contains a Mintlify documentation site for personal learning notes across software engineering topics.

## Structure

- `docs.json`: Mintlify site configuration, navigation, theme, icons, and footer links.
- `index.mdx`: Start page with cards for every learning track.
- `web/`, `dotnet/`, `c/`, `cloud/`, `databases/`, `container/`, `testing/`, `security/`, `processes/`, `miscellaneous/`: Published documentation pages.
- `images/content/`: Images and diagrams used by documentation pages.

## Development

Run the local Mintlify preview from the repository root:

```bash
npx mint dev
```

The preview usually opens at `http://localhost:3000`. If that port is occupied, Mintlify chooses the next free port, for example `http://localhost:3001`.

## Validation

Before publishing or exporting, run:

```bash
npx mint validate
npx mint broken-links
```

To build a static export:

```bash
npx mint export
```

The export command writes `export.zip` in the repository root.

## Content conventions

- Pages are MDX files with YAML frontmatter.
- Use sentence case for headings.
- Use active voice and second person where possible.
- Use Mintlify-native components such as `Card`, `Columns`, `AccordionGroup`, `Accordion`, `Steps`, `Tabs`, `Info`, `Warning`, and `Frame`.
- Use Font Awesome icon names. The site is configured with `"icons": { "library": "fontawesome" }`.
- Add page icons only when there is a clear semantic match. Leave weak matches out.
- Store local images under `images/` and reference them with root-relative paths.
