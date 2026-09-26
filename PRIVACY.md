# Privacy

mcplint is a local-first scanner. It does not collect, store, or transmit any
user data.

- **The plugin itself** runs no code and makes no network requests. It contains
  a skill that instructs Claude to run the pinned `mcplint` CLI on your machine.
- **mcplint scans local configuration files** to find MCP server definitions
  and to flag secrets hardcoded in them. File contents never leave the machine.
- **Online checks are off by default.** If you opt in (`--online`, or
  `online: true` in `.mcplint.yaml`), mcplint sends only the package name,
  ecosystem, and version of the MCP servers it finds to the OSV API
  (`https://api.osv.dev`) for CVE lookups. Nothing else is sent.
- **No telemetry, no accounts, no hosted service.**

Questions: open an issue at https://github.com/dtduc-git/mcplint/issues.
