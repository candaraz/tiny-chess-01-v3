# tiny-chess-01 v3

An original MIT chess engine in under 4,096 bytes of Python (packed).
0x88 board, PVS + LMR + transposition table + killers/history, guarded
null-move pruning, check extensions, capture quiescence, tapered
evaluation (piece tables, pawn structure, passed pawns, bishop pair,
rook files, pawn shield), repetition-aware search and root, fixed
per-opponent node budgets, and a small prepared book of first moves
for three scenarios (generated with the kit environment and this
engine's own search only). Deterministic: fixed node budgets, no wall
clock, no randomness, no model calls.

`main.py` is the packed entrypoint (kit `makefun compress` output);
`source.py` is the readable source it unpacks (kept uncommitted, sent
beside the transcripts as a pack).

Practice trial-0: 6/6, Elo 2112 (official scorer), verified locally
against the kit environment.
