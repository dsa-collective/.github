# dsa-collective

**Tools for understanding algorithms and data structures at a deeper level — finding bugs, classifying patterns, visualizing execution, analyzing complexity, and generating counterexamples.**

---

## What we're building

Most algorithm-learning tools stop at "correct or incorrect." dsa-collective goes further: when a solution is wrong, it explains *why* — which edge case broke it, which invariant was violated, which assumption didn't hold. When a solution is correct, it helps you see what's actually happening — which pattern you used, how its complexity was derived, and how the algorithm moves through data step by step.

Together, the repos form a toolkit for going from "my code passed" or "my code failed" to genuinely understanding the algorithm underneath.

## Repositories

| Repo | Description |
|---|---|
| [`dsa-autopsy`](https://github.com/dsa-collective/dsa-autopsy) | Finds bugs in incorrect algorithm solutions and explains failed edge cases, broken invariants, and invalid assumptions. |
| [`algorithm-pattern-classifier`](https://github.com/dsa-collective/algorithm-pattern-classifier) | Classifies solutions into algorithmic paradigms and patterns such as divide and conquer, dynamic programming, greedy, or sliding window. |
| [`algorithm-visualizer`](https://github.com/dsa-collective/algorithm-visualizer) | Visualizes the execution state of algorithms, including pointers, recursion, graphs, heaps, and dynamic-programming tables. |
| [`complexity-lab`](https://github.com/dsa-collective/complexity-lab) | Estimates and explains time and space complexity using static analysis and instrumented execution. |
| [`counterexample-generator`](https://github.com/dsa-collective/counterexample-generator) | Generates and minimizes inputs that expose differences between incorrect and reference solutions. |
| [`invariant-lab`](https://github.com/dsa-collective/invariant-lab) | Infers, validates, and visualizes invariants in loops, recursive algorithms, and data-structure operations. |

## How the repos work together

Each repo is independently useful and independently testable — you can drop any one of them into a project on its own. But they're designed to complement each other in a typical debugging/learning flow:

```text
A solution fails
      │
      ▼
counterexample-generator   → produces the smallest input that breaks it
      │
      ▼
dsa-autopsy                → explains which edge case / invariant / assumption failed
      │
      ▼
invariant-lab               → shows exactly where the loop or recursive invariant broke
      │
      ▼
algorithm-visualizer         → lets you watch the execution step by step to see it happen

A solution passes
      │
      ▼
algorithm-pattern-classifier → identifies which paradigm/pattern was used
      │
      ▼
complexity-lab                → derives and explains the time/space complexity
```

## Getting started

- Debugging a wrong solution? Start with [`dsa-autopsy`](https://github.com/dsa-collective/dsa-autopsy) or [`counterexample-generator`](https://github.com/dsa-collective/counterexample-generator).
- Want to see an algorithm run step by step? [`algorithm-visualizer`](https://github.com/dsa-collective/algorithm-visualizer) is the place to look.
- Trying to understand complexity or pattern recognition for a solution that already works? [`complexity-lab`](https://github.com/dsa-collective/complexity-lab) and [`algorithm-pattern-classifier`](https://github.com/dsa-collective/algorithm-pattern-classifier) cover that.

## Contributing

We welcome contributions across all repositories — new algorithm coverage, additional invariant patterns, visualization improvements, and documentation. See each repository's `CONTRIBUTING.md` for specifics, or the shared guidelines in this organization's [`.github`](https://github.com/dsa-collective/.github) repo.
