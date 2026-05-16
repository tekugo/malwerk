# malwerk

A modal, vi-style terminal drawing/diagramming tool built on the
[zeichenwerk](https://github.com/tekugo/zeichenwerk) TUI framework.
Draw boxes, lines, and annotations on a cell grid; modes for normal,
insert, visual, and extended commands; junction-aware line drawing;
undo/redo with history; save to `.malwerk.json` and load back.

## Install

```sh
go install github.com/tekugo/malwerk@latest
```

## Run

```sh
malwerk                       # blank canvas at terminal size
malwerk drawing.malwerk.json  # open an existing drawing
malwerk -w 120 -h 40          # custom initial canvas size
malwerk -t nord               # pick a theme
```

Themes: `tokyo` (default), `gruvbox-dark`, `gruvbox-light`, `nord`,
`lipstick`, `midnight`.

## Modes

vi-style modal interface. From normal mode, `i` to insert, `v` for
visual selection, `:` for extended commands. `Esc` returns to normal.

## File format

Drawings are stored as JSON with the `.malwerk.json` extension. The
file is a snapshot of the canvas grid plus metadata; it round-trips
through load/save losslessly.

## Status

Early — extracted from `cmd/malwerk` in the zeichenwerk monorepo as
a standalone tool. API and shape may change without notice.

## License

MIT — same as the upstream zeichenwerk library.
