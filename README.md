# Degrees of Separation

A Python command-line program that finds a connection between two actors through movies in which they appeared together.

The project models actors and movies as a graph, then uses breadth-first search to look for a path from one person to another.

## Requirements

- Python 3
- No third-party packages

## Run

Use the small dataset for a quick test:

```sh
python3 degrees.py small
```

Or use the larger included dataset:

```sh
python3 degrees.py large
```

If no directory is supplied, the program uses `large` by default. Enter two actor names when prompted. When a name is ambiguous, choose the intended person by ID.

## Data layout

Both `small/` and `large/` contain:

- `people.csv` — actor IDs, names, and birth years
- `movies.csv` — movie IDs, titles, and years
- `stars.csv` — actor-to-movie relationships

## Implementation

- `degrees.py` loads the CSV data, resolves names, builds graph neighborhoods, and performs the search.
- `util.py` provides stack, queue, and priority-queue helper classes.

## Status

Breadth-first search is the active shortest-path implementation. Alternative depth-first and A* functions are present as experiments but are not used by the command-line flow.
