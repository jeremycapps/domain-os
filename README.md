# domain-os

A local-first operating system that mounts protocol-defined context as an agent-navigable filesystem.

Domain OS owns the mounted filesystem.

Protocol repos define objects and address grammar. Domain OS turns them into files.

## Core split

```text
Libera = address grammar
Domain = semantic binding
Timpos = replayable moments
Corus = objective satisfaction
Facia = active use
Runtime = existence checks and execution
```

## Filesystem rule

Only Domain OS owns filesystem structure.

```text
Libera defines paths.
Domain binds paths to meaning.
Timpos records state changes at paths.
Corus evaluates requirements over paths.
Facia routes active conditions into use.
Domain OS mounts the result as files.
```

## Path to filesystem

Libera path:

```text
movement/change/facia_surface_model.status
```

Domain OS mounted file:

```text
programs/protocol_design/libera/movement/change/facia_surface_model/status.yaml
```

Domain binding:

```text
programs/protocol_design/domain/bindings/facia_surface_model_change.yaml
```

Corus requirement:

```text
programs/protocol_design/corus/objectives/facia_v2/requirements/surface_model_updated.yaml
```

Facia active surface:

```text
programs/protocol_design/facia/surfaces/implement/surface_model_updated.yaml
```

## Domain binding

A domain binding connects Libera motion to domain semantics.

```yaml
binding:
  id: binding.facia_surface_model_change
  domain: domain.protocol_design

  libera:
    pressure: movement
    operation: change
    slot: facia_surface_model.status

  type: schema_change

  execution:
    object: facia_schema
    action: replace_surface_model

  meaning:
    why: Facia should own use, not duplicate Libera pressure or domain type.
    for:
      - context_rebuild_agent
      - future_repo_maintainer
```

## Runtime responsibility

The runtime prevents agents from treating missing context as accepted state.

Before an agent can cite or act on context, the runtime should resolve:

```text
Does the file exist?
Does the binding exist?
Does the source exist?
Does the prior moment exist?
Does the objective reference the requirement?
Does the condition resolve?
Does the surface route exist?
```

## Keeper

```text
Protocol repos define objects.
Domain OS mounts them as files.

Libera defines addresses.
Domain gives addresses meaning.
Corus evaluates objective state.
Facia exposes active use.
Runtime enforces existence.
```
