# Effect-TS Skills

A collection of AI-powered skills for [Effect-TS](https://effect.website/) development, compatible with [skills.sh](https://skills.sh).

## Installation

```bash
npx skills add mrevanzak/effect-ts-skills
```

Or install individual skills:

```bash
npx skills add mrevanzak/effect-ts-skills/effect-ts-fundamentals
npx skills add mrevanzak/effect-ts-skills/effect-ts-errors
npx skills add mrevanzak/effect-ts-skills/effect-ts-resources
npx skills add mrevanzak/effect-ts-skills/effect-ts-concurrency
npx skills add mrevanzak/effect-ts-skills/effect-ts-anti-patterns
```

## Skills Overview

| Skill | Description | Use When |
|-------|-------------|----------|
| **effect-ts-fundamentals** | Service pattern, Effect.gen, Layers | Starting with Effect-TS, defining services |
| **effect-ts-errors** | TaggedError, catchTag, error accumulation | Implementing error handling, validation |
| **effect-ts-resources** | acquireRelease, Scope, cleanup | Managing DB connections, file handles |
| **effect-ts-concurrency** | Fiber, Semaphore, Deferred, bounded parallelism | Parallel operations, rate limiting |
| **effect-ts-anti-patterns** | Common mistakes and fixes | Code review, debugging crashes |

## Skill Dependency Graph

```
effect-ts-fundamentals (start here)
    |
    +---> effect-ts-errors
    |
    +---> effect-ts-resources
    |
    +---> effect-ts-concurrency
              |
              v
       effect-ts-anti-patterns
```

## Key Patterns Covered

### Core Concepts
- Modern Service Pattern with `Effect.Service`
- Generator-based composition with `Effect.gen` and `yield*`
- Layer-based dependency injection

### Error Handling
- Type-safe errors with `Data.TaggedError`
- Selective error handling with `Effect.catchTag`
- Error accumulation with `{ mode: 'either' }`

### Resource Management
- Guaranteed cleanup with `Effect.acquireRelease`
- Scoped resources with `Effect.scoped`
- LIFO cleanup order

### Concurrency
- Bounded parallelism with `{ concurrency: n }`
- Rate limiting with `Semaphore`
- Inter-fiber signaling with `Deferred`

### Anti-Patterns
- Missing `yield*` trap
- Running effects outside boundaries
- Unbounded parallelism
- Using `throw` instead of `Effect.fail`

## Source

Based on patterns from [EffectPatterns](https://github.com/PaulJPhilp/EffectPatterns).

## License

MIT
