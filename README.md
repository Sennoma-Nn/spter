# spter - Terminal Separator Generator

A lightweight shell script that generates adaptive-width horizontal separators in the terminal with customizable string and dynamic line overwriting capability.

## Features

- **Adaptive Width**: Automatically adjusts to your terminal width
- **Customizable String**: Use any single string as separator
- **Line Overwriting**: Option to overwrite previous lines for cleaner output
- **Lightweight**: Single-file implementation with no dependencies

## Installation

1. Make the script executable:
```shell
chmod +x spter
```

2. Move it to your local bin directory (recommended):
```shell
mkdir -p ~/.local/bin
mv spter ~/.local/bin/
```

3. Ensure `~/.local/bin` is in your PATH (add to your shell config if needed):
```shell
export PATH="$HOME/.local/bin:$PATH"
```

## Usage

### Basic Usage
```shell
spter
```
Generates a horizontal line using the default string (`-`) that spans the full terminal width.

### Custom String
```shell
spter -s "*"
```
Generates a separator using the specified string.

### Overwrite Prompt Line
```shell
spter -c 1
```
Overwrites the current prompt line before printing the separator. This creates cleaner output by removing the prompt from view.

**Usage:**
- `-c 0` or no cover option: Separator appears below the prompt
- `-c 1`: Separator overwrites the prompt line for cleaner output

## Examples

```shell
# Simple separator
spter

# Double line separator
spter -s "="

# Star separator overwriting 2 previous lines
spter -s "*" -c 2

# Using short options
spter -s "#" -c 1
```

## License

This project is licensed under the BSD 3-Clause License - see the [LICENSE](LICENSE) file for details.
