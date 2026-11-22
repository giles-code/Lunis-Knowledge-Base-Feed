# Lunis Knowledge Base Feed

The public website feed for the **Reference Library** on the Lunis Partners website. It contains one file,
`kb-data.json`, which the Reference Library pages read from:

```
https://raw.githubusercontent.com/giles-code/Lunis-Knowledge-Base-Feed/main/kb-data.json
```

**Do not edit anything here.** The file is generated from the private Lunis Knowledge Base repository. On every
merge to its `main` branch, a GitHub Action rebuilds the file from **approved entries only** and commits it here.
Draft and in-review content never appears in this repository.

## What is in the file

| Part | One item per | Main fields |
|---|---|---|
| `sectors` | Sector | `_id`, `label`, `order` |
| `topics` | Topic | `_id`, `label`, `order` |
| `concepts` | Approved concept (a glossary term, with its acronyms) | `_id`, `term`, `acronyms`, `aliases`, `sectors`, `shortDefinition`, `bodyHtml`, `sectorNotes`, `jurisdictions`, `sourcesHtml`, `related`, `explainers`, `lastReviewed`, `searchKeys` |
| `acronyms` | Acronym of an approved concept | `acronym`, `conceptId`, `term`, `sectors`, `notes`, `searchKeys` |
| `explainers` | Approved explainer | `_id`, `title`, `summary`, `bodyHtml`, `sectors`, `topics`, `concepts`, `sourcesHtml`, `lastReviewed` |
| `resources` | Approved framework guide, governance toolkit item or authority profile | `_id`, `kind`, `title`, `summary`, `bodyHtml`, `sectors`, `topics`, `concepts`, `lastReviewed` |

`generated` gives the build date and `status` is always `approved`. Field definitions are in the Lunis Knowledge
Base README.
