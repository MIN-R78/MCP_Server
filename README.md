# MCP_Server

A minimal example of an MCP server implemented in Python using stdin/stdout communication.

## Project Structure
```
MCP_Server/
- mcp-server.py        # Main server script that registers tools and runs stdio_server
- check-test.py        # Client script for testing the server
- my_mcp_server/
│   ├── __init__.py
│   └── stdio_server.py  # Reads JSON input and returns output
```

## How to Run
```bash
python check-test.py
```

### Example Output
```
Starting MCP server...
Calling stdio_server...
[DEBUG] add called with x=5, y=7
{"output": 12}
```

## Input Format
```json
{
  "tool": "simple_adder",
  "function": "add",
  "inputs": {
    "x": 5,
    "y": 7
  }
}
```

## Requirements
- Python 3.x
- No external dependencies

