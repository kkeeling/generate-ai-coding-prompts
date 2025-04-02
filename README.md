# Prompt Generator

This script generates a structured AI coding prompt based on a provided feature specification and optional context. The generated output is displayed on standard output.

## Requirements

- Python >= 3.12
- [Click](https://palletsprojects.com/p/click/) library. Install it via pip:

  ```sh
  pip install click
  ```

## Script Overview

The `prompt-generator.py` script is a command-line tool that takes a feature name as a positional argument along with optional specification and context files. It uses these inputs to generate a coding prompt using a predefined template.

The script performs the following tasks:

1. Reads the feature specification from a file (using the `--spec-file` or `-f` flag) or from standard input if no spec file is provided.
2. Optionally reads additional context from a file using the `--context-file` or `-c` flag.
3. Formats the prompt according to a predefined template and outputs the result to the terminal.

## Usage

### Command Syntax

```sh
uv prompt-generator.py FEATURE_NAME [--spec-file SPEC_FILE] [--context-file CONTEXT_FILE]
```

- `FEATURE_NAME`: The name of the feature for which the prompt is generated.
- `--spec-file` or `-f`: (Optional) Path to the file containing the feature specification.
- `--context-file` or `-c`: (Optional) Path to the file containing additional context.

### Examples

#### Example 1: Using a specification file

If you have a spec file named `spec.md`:

```sh
uv prompt-generator.py "User Authentication" -f spec.md
```

#### Example 2: Using both specification and context files

If you have both spec and context files:

```sh
uv prompt-generator.py "API Integration" -f spec.txt -c context.txt
```

#### Example 3: Reading specification from standard input

If no spec file is provided, the script will prompt you to enter the feature specification directly. End your input using Ctrl+D (or Ctrl+Z in Windows):

```sh
uv prompt-generator.py "Data Processing"
```

After executing the command, type your specification and then signal the end of input with Ctrl+D.

## How It Works

1. **Input Handling:**
   - Accepts a feature name as a positional argument.
   - Optionally reads the spec file and context file if provided.

2. **Prompt Formatting:**
   - Uses a predefined template that incorporates the feature name, specification, and optional context.

3. **Output:**
   - Generates a coding prompt and prints it to the terminal.

## License

(Include license information here, if applicable.)

## Contributing

(Instructions for contributing can be added here.) 