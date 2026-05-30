# Trae Tool Mapping

Skills use Claude Code tool names. When you encounter these in a skill, use your platform equivalent:

| Skill references | Trae equivalent |
|-----------------|----------------------|
| `Read` (file reading) | `Read` |
| `Write` (file creation) | `Write` |
| `Edit` (file editing) | `SearchReplace` |
| `Bash` (run commands) | `RunCommand` |
| `Grep` (search file content) | `Grep` |
| `Glob` (search files by name) | `Glob` |
| `TodoWrite` (task tracking) | `TodoWrite` |
| `Skill` tool (invoke a skill) | `Skill` |
| `WebSearch` | `WebSearch` |
| `WebFetch` | `WebFetch` |
| `Task` tool (dispatch subagent) | `general_purpose_task` (see [Subagent support](#subagent-support)) |

## Subagent support

Trae supports subagents via specialized tools. Use `general_purpose_task` for most workflow dispatches.

| Skill instruction | Trae equivalent |
|-------------------|----------------------|
| `Task tool (superpowers:implementer)` | `general_purpose_task` with the filled `implementer-prompt.md` template |
| `Task tool (superpowers:code-reviewer)` | `TRAE-code-review` (platform skill) or `general_purpose_task` |
| `Task tool (search)` | `search` (specialized agent) |
| `Task tool (general-purpose)` | `general_purpose_task` |
