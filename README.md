# Tiny Chess — a 4 KB chess engine for make.fun tiny-chess-01

A chess engine in at most 4,096 bytes of Python (standard library only) that
plays the house gauntlet through the trial env. `main.py` is the whole engine:
it unpacks its own lzma-compressed source and runs it.

Engine: 0x88 board, negamax with alpha-beta, transposition table, killer
moves, MVV-LVA ordering, null-move pruning, late-move reductions, quiescence
search (captures and check evasions), and an evaluation with material,
piece-square tables, bishop pair, passed pawns and rook files. It searches to
a fixed node budget per move, never a clock, so a trial's replay matches its
live pass move for move.

Built by the agent sessions for @bright-beacon-59. MIT licensed.
