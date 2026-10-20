---
name: ponytail-pr
description: >
  Style for pull request titles and descriptions. Use whenever writing or
  revising a PR title or body: "PR 올려", "PR 메시지", "PR 설명 써줘",
  `gh pr create`, `gh pr edit`. Korean by default, feature-area bullets,
  compact noun endings. Fork-local addition (kingsj0405/ponytail), adapted
  from a teammate's AGENTS.md.
---

# PR title and description style

## Language

- When the user does not specify a language, write PR titles and descriptions in Korean.
- When the user explicitly specifies a language, use that language instead. English is the likely alternative, but do not assume English without an explicit request.

## Form

- Organize the description by feature area with short Markdown bullet points.
- Lead each top-level bullet with the problem, operational context, or reason for the change when it is not self-evident.
- Put only the core implementation or behavior under concise nested bullets.
- Prefer compact noun endings in Korean, such as `개선`, `변경`, `추가`, `제거`, and `확인`.
- Avoid unnecessary `~함` endings when a noun ending is natural. For example, use `사용성 개선`, `구현 변경`, and `복구 처리 추가`.
- Use `~함` only when removing it would make the sentence awkward or ambiguous.
- Do not use the middle dot character, em dash, or en dash. Use commas, parentheses, normal prose, and Markdown hyphen bullets instead.
- Keep technical identifiers in backticks and preserve exact names, flags, counts, test denominators, and baseline versus regression distinctions.
- Prefer a compact feature summary over a file-by-file change list.

## Content

- Describe the PR as a whole, not just the latest commit, with a concise summary of the core features and behavior changes.
- When needed to understand behavior, include brief representative inputs and results, distinguishing observed results from synthetic examples or expected behavior.
- Briefly state the validation performed and its results, noting any unverified scope or application limits that affect interpretation.
- Explain relevant dependencies or scope boundaries only when needed for review.

## Precedence

A repository's own PR rules (its `AGENTS.md`, `CLAUDE.md`, or a PR command such
as `/upstream-pr`) win over this skill. Apply this skill to whatever those rules
leave open, for example the form of a body they allow to be long.

## Example

~~~markdown
### 에이전트와 trajectory

- 5개 scaffold 사용성 개선
  - 대상 scaffold는 Claude Code, Hermes, OpenCode, Pi, mini-swe
  - 원격 환경 실행을 위한 host-run agent 구현 변경
  - compaction 처리 및 ATIF 포맷 export 구현
- Terminus 2의 `tmux not found` 오류 해결을 위한 portable tmux 연결 추가
~~~
