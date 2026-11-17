# jubilant-waffle

A lightweight command-line tool for keeping running tallies of anything: counts, expenses, scores, habits.

![license](https://img.shields.io/badge/license-MIT-blue)
![python](https://img.shields.io/badge/python-3.10%2B-blue)

jubilant-waffle lets you create named tallies, add to them from the terminal, and see totals at a glance. Data is stored locally in a single JSON file, so there is no account, server, or setup.

## Features

- Create as many named tallies as you need
- Add or subtract values with one short command
- View totals, history, and simple summaries
- Export to CSV
- Local-only storage, no network required

## Installation

```bash
git clone https://github.com/your-username/jubilant-waffle.git
cd jubilant-waffle
pip install -e .
```

Requires Python 3.10 or newer.

## Usage

```bash
# Create a tally
tallyo new coffee

# Add to it
tallyo add coffee 1
tallyo add coffee 2

# Subtract
tallyo sub coffee 1

# Show the total
tallyo show coffee
# coffee: 2

# List all tallies
tallyo list

# See history
tallyo log coffee

# Export to CSV
tallyo export coffee --out coffee.csv

# Reset a tally
tallyo reset coffee
```

Run `tallyo --help` for all commands and options.

## Configuration

By default, data is stored at `~/.tallyo/data.json`. To use a different location, set the environment variable:

```bash
export TALLYO_DATA=/path/to/data.json
```

## Project Structure

```
jubilant-waffle/
├── src/tallyo/
│   ├── cli.py
│   ├── storage.py
│   └── __init__.py
├── tests/
├── pyproject.toml
├── README.md
└── LICENSE
```

## Development

```bash
pip install -e ".[dev]"
pytest
```

## Roadmap

- [ ] Tags and categories
- [ ] Weekly and monthly summaries
- [ ] Optional sync between devices

## Contributing

Contributions are welcome. Please open an issue to discuss larger changes before submitting a pull request, and include tests for new behavior.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
