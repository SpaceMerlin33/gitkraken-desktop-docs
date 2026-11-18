# gitkraken-desktop-docs

Source files for the GitKraken Desktop documentation: new features, how-to guides, integration setup, troubleshooting, and release notes. To read the published docs, go to the [GitKraken Help Center](https://help.gitkraken.com/gitkraken-desktop/gitkraken-desktop-home/).

## What's in this repo

| Path | Contents |
| --- | --- |
| `gitkraken-desktop/` | One Markdown file per Help Center page. Each page is published at `help.gitkraken.com/gitkraken-desktop/<slug>/`. |
| `gitkraken-desktop/GKD-New-Page-Template.md` | Starting template for a new page, including the required front matter. |
| `_images/` | Images referenced by pages. |
| `llms.txt`, `llms-full.txt` | Indexes of the docs for AI tools, built from page front matter. |
| `sitemap.xml` | Sitemap of the published pages. |
| `pull_request_template.md` | Template applied to new pull requests. |

The docs cover:

- **New features**, such as coding agents, worktrees, and GitKraken AI.
- **How-to guides** for everyday Git work: committing, branching, merging, rebasing, stashing, and pull requests.
- **Integrations** with GitHub, GitLab, Bitbucket, Azure DevOps, Jira, and Trello.
- **Self-hosted and Enterprise** installation and configuration.
- **Troubleshooting**, FAQs, and release notes (`current.md` and the version archives such as `11x.md`).

## Contributing

1. Create a branch from `main`.
2. Edit an existing page in `gitkraken-desktop/`, or copy `GKD-New-Page-Template.md` to start a new one. Every page needs the front matter fields shown in the template.
3. Run the page checker and fix every `ERROR` before you open a pull request:

   ```sh
   python .claude/skills/gkhc-docs-authoring/scripts/check_pages.py gitkraken-desktop/<page>.md
   ```

   Run it with no arguments to check every page and the full navigation hierarchy.4. Open a pull request into `main` and fill in the template.

The full authoring rules (front matter schema, page types, Markdown patterns, callouts, and how renames and archives publish) are in [`.claude/skills/gkhc-docs-authoring/SKILL.md`](.claude/skills/gkhc-docs-authoring/SKILL.md).
