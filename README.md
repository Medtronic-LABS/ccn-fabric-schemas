# ccn-fabric-schemas

The **single source of truth** for the CCN fabric: the domain schemas, message and
action shapes, and network/registry configuration that every node on the network
agrees on. The reference CC system and all edge coordinators consume a **pinned
release** of this repo.

## Layout

```
schemas/
  domains/     # care-coordination domain objects (referral, encounter, patient ref, …)
  registry/    # network/registry config: nodes, roles, endpoints
  examples/    # sample messages used in tests and docs
```

## Principles

- **Authoritative.** If the architecture doc and these schemas disagree, the schemas win.
- **Versioned.** Semantic versioning; published as a release/package so consumers can pin.
- **Generated, not copied.** Consumers should generate types from these schemas rather
  than hand-maintaining duplicates.

## TODO before first release

- [ ] Pick the schema language (JSON Schema / OpenAPI / Protobuf) — record as an ADR.
- [ ] Define the action set and the care-coordination domain objects.
- [ ] Add codegen + a published package per target language.
- [ ] Set up schema validation in CI.

## License

TODO: align with the org standard.
