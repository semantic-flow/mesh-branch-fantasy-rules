# mesh-branch-fantasy-rules

`mesh-branch-fantasy-rules` is the branch-published fixture repository for the Fantasy Rules Semantic Flow ladder.

The normal source branch stays clean: authored source files and deterministic replay assets live here, while generated Semantic Flow mesh output is published from a separate branch such as `gh-pages`.

Current replay source refs:

- `a.00-blank-slate`
- `a.01-source-only`

Publication rungs should be generated as commits on the publication branch rather than merged into `main`. Matching `a.*-woven` refs mark accepted publication checkpoints so the whole ladder alpha-sorts in numeric order.

Current accepted publication coverage runs through `a.15-extracted-term-references-woven`, with `gh-pages` fast-forwarded to that state. The fixture covers publication bootstrap, repository-backed ontology/SHACL/example materialization, named release weaving, all-term extraction, broad ResourcePage generation, `_knop/_sources` provenance, and representative current-mode canonical references.

Source ownership:

- Accord manifests live in the Semantic Flow Framework conformance example.
- Replay source bytes live in this repository under `.assets/`.
- `main` carries clean authored source files. `a.00-blank-slate` carries source-control material and deterministic replay assets, but no generated mesh output.
- Generated publication output is disposable replay output.

Publication output records source provenance beside each target Knop. Repository-backed source bindings and extraction-source details live in `_knop/_sources/sources.ttl`, linked from the Knop inventory with `sflo:hasKnopSourceRegistry`; curated references live separately in `_knop/_references/references.ttl`.

Regeneration is local-only by default in Weave's fixture ladder tooling; pushing branch updates is an explicit follow-up step. For local preview/regeneration, `WEAVE_LOG_DIR=/tmp/weave-logs` keeps runtime logs outside the publication tree.
