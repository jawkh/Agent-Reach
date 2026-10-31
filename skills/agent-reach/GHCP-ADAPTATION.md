# GHCP adaptation notes (agent-reach)

Packaged for GitHub Copilot CLI from upstream commit 14c213405669414492bda0f8d52cc6531d062c45 (MIT, Agent Eyes).

Adaptations
- `SKILL.md` is `agent_reach/skill/SKILL_en.md` rendered with `agent_reach.runtime.manage.render_skill('en')` (version 1.6.0, channel table filled in).
- Removed `agent-reach setup` install-report section and the `agent-reach skill link` row.
- `agent-reach update` and `meta.update` handling replaced with a pointer to `/sync-upstream-ghcp-fork`; `references/maintenance.md` updated the same way.
- Added a "GHCP install notes" section: never run `setup`, `update`, or `skill link`.

Parity report
- read/search channels: preserved (CLI pinned via pipx).
- automatic activation by description: preserved.
- dedicated browser + login reuse: preserved (`agent-reach browser status`).
- setup install report: omitted (setup writes ~/.agents and ~/.claude skill folders); accepted.
- in-place update: degraded (sync via /sync-upstream-ghcp-fork); accepted.
- skill link for other AIs: omitted; accepted.
