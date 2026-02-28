# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-file browser-based Tic Tac Toe game. No build step, no dependencies, no package manager.

**To run:** open `tictactoe.html` directly in a browser.

## Architecture

Everything lives in `tictactoe.html` — inline CSS, HTML, and a `<script>` block.

**Key state variables:**
- `board` — 9-element array of `''`, `'X'`, or `'O'`
- `current` — whose turn it is (`'X'` or `'O'`)
- `over` — boolean, blocks clicks after game ends
- `scores` — `{X, O, D}` object, persists across restarts

**Core functions:**
- `init()` — resets board/state, called on page load and Restart button
- `checkWinner()` — checks `WINS` constant (all 8 winning lines) against `board`; returns `{winner, line}` or `null`

**CSS classes on `.cell`:** `x`/`o` (color), `taken` (blocks hover), `winner` (highlight + pulse animation)

## Git Workflow

- Commit and push after every meaningful change
- Use imperative commit messages (e.g. `"Add AI opponent"`, `"Fix draw detection bug"`)
- Push immediately after committing: `git push`
- GitHub repo: https://github.com/adambirnbaum/hello-world
