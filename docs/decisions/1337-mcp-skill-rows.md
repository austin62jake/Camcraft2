## #1337, #1343, #989 - camcraft-mcp skill: set_operation_coolant, edit_tool, thread mills (2026-11-13)

- **Chosen: one process PR for three owed skill entries.** #1343 suggests riding with #1337, and #989 edits the
  same file; one PR bumps `PROCESS_VERSION` once (52 -> 53) instead of three PRs racing for the same number
  (#1153). #1356 (`electrode_from_faces`) is left for later: its tool's PR #1156 has not merged.
- **Chosen: the rows say what main implements, read from the code and its tests.** `edit_tool` takes `patch`
  (not `definition`) and refuses `number` / `body` / `cutter`; `set_operation_coolant` reads its word
  case-blind and warns, rather than refuses, on a mode the machine has no coded entry for; the Thread note quotes
  the refusals `crates/app/tests/mcp.rs` pins (`thread_milling_over_the_tools`). The Thread note also names the
  `external` param (#985) in one clause, since it shapes the same operation.
- **Dropped:** a separate "tool kinds" section (the skill has none; the thread-mill kinds sit beside `add_tool`,
  where an agent reads the definition shape).
