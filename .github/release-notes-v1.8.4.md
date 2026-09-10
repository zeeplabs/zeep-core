## v1.8.4

Patch release fixing the generated OpenAPI/Swagger documentation for the list endpoint, which was missing filter and soft-delete syntax.

### Fixed

- **`GET /{app}/{table}` list endpoint docs missing filter and soft-delete syntax.** The list endpoint already supported per-column filtering (`?column=operator.value`, operators `eq.`/`ne.`/`gt.`/`gte.`/`lt.`/`lte.`/`like.`/`ilike.`/`in.`) and a `deleted` toggle to include soft-deleted rows, but the generated OpenAPI spec only documented `limit`/`offset`/`order`. Both are now documented on the list operation, including a note that unknown query parameters return `400` and that `deleted` only accepts the literal value `true`.

### Upgrade notes

Documentation-only change — no behavior changed, no migration needed, no breaking changes.
