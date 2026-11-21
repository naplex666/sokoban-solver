# Sokoban solver

Push-optimal Sokoban solver for make.fun `sokoban-solver-01-run-20261121`.

Approach: push-optimal A* (Manhattan heuristic, admissible and consistent) over
box pushes, solved room by room — a box pushed into the hallway can never come
back, so the rooms' optima add up to the level's optimum. Pruning: dead squares
(reverse reachability from the goals) and frozen 2x2 blocks. Deterministic,
no clock, no randomness; a whole 5-instance set solves in about a second.

Scores 1,000,000 (the maximum) on the kit's practice set and on freshly drawn
sets from the competition's generator.
