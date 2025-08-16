# MCP Client – Airbnb & Weather Tools 🌍🏡

This project demonstrates how to use the **Model Context Protocol (MCP)** to interact with external MCP servers and expose useful tools. It includes an Airbnb client integration and a weather utility.

## 📂 Project Structure

```
.
├── .gitignore
├── .python-version
├── README.md
├── client.py        # MCP client for Airbnb server
├── main.py          # Entry point / orchestration
├── pyproject.toml   # Project metadata & dependencies
├── uv.lock          # Lockfile for reproducible environments
└── weather.py       # MCP tool for fetching weather info
```

## ⚡ Features

* **Airbnb MCP Client**

  * Connects to the [OpenBnB MCP server](https://www.npmjs.com/package/@openbnb/mcp-server-airbnb).
  * Lists available MCP tools.
  * Runs `airbnb_search` to fetch results (example: search for rentals in California).

* **Weather Tool**

  * Fetches weather information (extendable for forecasts, locations, etc.).

* **MCP Integration**

  * Uses `ClientSession` and `stdio_client` to communicate with external MCP servers.
  * Demonstrates tool discovery and invocation.

## 🔧 Usage

1. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Run the Airbnb client:

   ```bash
   python client.py
   ```

3. Example output:

   ```
   Starting stdio_client...
   Client connected, creating session...
   Initializing session...
   Listing tools...
   Available tools: [...]
   Calling tool...
   Tool result: { ... }
   ```

4. Run other tools (example):

   ```bash
   python weather.py
   ```

## 🌐 References

* [Model Context Protocol (MCP)](https://github.com/modelcontextprotocol)
* [OpenBnB MCP Server](https://www.npmjs.com/package/@openbnb/mcp-server-airbnb)
