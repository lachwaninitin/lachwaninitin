# Heap Analysis Skill for Claude Code

A Claude Code skill for analyzing Java heap dumps (hprof files) to count instances of specific classes.

## Installation

1. Copy this directory to your Claude Code skills folder:
```bash
cp -r heap-analysis ~/.claude/skills/
```

2. Restart Claude Code or reload skills

## Usage

```bash
/heap-analysis <class-name> [directory]
```

### Examples

```bash
# Analyze PayloadHopper instances in current directory
/heap-analysis com.salesforce.eventbus.slingshot.util.avro.PayloadHopper

# Analyze in specific directory
/heap-analysis com.example.MyClass /path/to/dumps
```

## Features

- Parses Java heap dump (.hprof) files
- Counts instances of specified classes (including inner classes)
- Generates formatted markdown tables with results
- Shows file sizes and statistics
- Identifies patterns across multiple heap dumps

## Requirements

- Python 3.6+
- No external dependencies (uses only standard library)

## Output

Returns a table showing:
- File name
- Instance count per file
- File size
- Summary statistics and patterns

## License

MIT
