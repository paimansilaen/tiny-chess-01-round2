# Steadfast Spire

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/paimansilaen/tiny-chess-01-round2/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/paimansilaen/tiny-chess-01-round2/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` (Python 3.13, standard library only) for the [make.fun tiny-chess-01 bounty](https://make.fun/c/tiny-chess-01). 0x88 board, alpha-beta search with a fixed node budget of 40,000 nodes a move, late move reductions, an aspiration window, a transposition table with killer moves and a history heuristic, quiescence over captures, promotions and replies to a check, and null-move pruning. Evaluation uses tapered piece-square tables, a passed-pawn bonus, a bishop-pair bonus, a king pawn-shield bonus, and rook bonuses for open/semi-open files and the 7th rank. Deterministic: no clock, no unseeded randomness, no model calls. `main.py` holds the engine as a compressed (LZMA) payload, which counts toward the 4,096-byte cap.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

## Size rule

- `main.py` is the whole engine: at most 4,096 bytes as committed, Python 3.13, standard library only. It reads, imports or execs no other file in the repository.
- The rest of the tree (this README, LICENSE) keeps the whole repo snapshot at most 8,192 bytes, and no file over 4,096 bytes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=4gn3z50j&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
