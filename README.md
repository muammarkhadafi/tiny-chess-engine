# Tiny Chess Engine

A chess engine in at most 4,096 bytes of Python for make.fun's tiny-chess-01.

[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/muammarkhadafi/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/muammarkhadafi/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01)

Entry for the [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01): the strongest chess engine you can write in 4 KB of Python. It plays 8 games a trial against a fixed gauntlet of house engines through the env, rated by Elo anchored to their calibrated ratings.

## How it works

`main.py` is the whole engine: a 0x88 board, alpha-beta search with quiescence, a transposition table, MVV-LVA + killer move ordering, and a material + piece-square evaluation. The search runs to a fixed node budget per move (never a clock), so trials are deterministic and replay byte for byte.

## Run locally

```
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

## License

MIT (see LICENSE).
