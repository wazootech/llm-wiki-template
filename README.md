# LLM Wiki template

Opinionated [LLM Wiki](https://github.com/wazootech/wiki/blob/main/docs/wiki/LLM_Wiki.md) starter — agent gardening, SHACL shapes, and SPARQL-backed indexes. Distinct from the generic [`wiki-template`](https://github.com/wazootech/wiki-template).

Registry: [Wiki CLI templates](https://github.com/wazootech/wiki/blob/main/docs/wiki/Wiki_CLI.md#ecosystem-templates).

## Quick start

```bash
pip install wazootech-wiki
wiki check --strict
wiki serve --watch
```

Read [wiki/LLM_Wiki_Guide.md](wiki/LLM_Wiki_Guide.md) for agent workflows (`check`, `lint`, `fmt`, `render`, `link`).

## Agent hygiene

- Run `wiki check --strict` before commit; `wiki lint --strict` for conventions.
- Run `wiki fmt` on edited markdown.
- Use `wiki render` to refresh embedded SPARQL tables.
- See [AGENTS.md](AGENTS.md) for coding-agent instructions.

## Layout

- `wiki.yaml` — `graph.content_predicate: schema:articleBody`, standard prefixes
- `wiki/Person_Shape.md`, `wiki/Concept_Shape.md` — SHACL shapes
- `wiki/LLM_Wiki_Guide.md` — gardening and agent DX
- `wiki/Ethan_Davidson.md` — example person page

## Deploy

Enable GitHub Pages (GitHub Actions). The [deploy-pages workflow](.github/workflows/deploy-pages.yml) runs `wiki build`.

## Related

- [Wiki CLI](https://github.com/wazootech/wiki)
- [LLM Wiki pattern](https://github.com/wazootech/wiki/blob/main/docs/wiki/LLM_Wiki.md)
