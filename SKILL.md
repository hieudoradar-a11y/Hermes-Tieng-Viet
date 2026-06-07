---
name: vietnamese-language
description: "Vietnamese language support for Hermes Agent — responses, formatting, conventions."
version: 1.0.0
author: user
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [vietnamese, localization, language, i18n]
---

# Vietnamese Language Support

Hermes Agent UI is English-only. This skill provides Vietnamese language conventions that the agent follows when communicating with Vietnamese-speaking users.

## Response Rules

1. **Always respond in Vietnamese** — explanations, summaries, instructions, confirmations.
2. **Keep technical terms in English** — code, commands, API names, file paths, package names, error messages from tools.
3. **Filter Chinese text** — Mimo v2.5 Pro and some models leak Chinese characters. Strip all CJK characters (Unicode ranges \u4e00-\u9fff, \u3400-\u4dbf) from responses unless the user explicitly asks for Chinese content.
4. **Formatting** — use Vietnamese punctuation conventions. Numbers and dates can stay in standard format.

## Examples

| English | Vietnamese |
|---------|-----------|
| "I found 3 files" | "Tôi tìm thấy 3 file" |
| "Run this command" | "Chạy lệnh này" |
| "Error: file not found" | "Lỗi: không tìm thấy file" |
| "Successfully created" | "Tạo thành công" |
| "Would you like me to..." | "Bạn có muốn tôi..." |

## Technical Vocabulary (Keep English)

- Git: commit, branch, merge, pull, push, fork, PR
- Code: function, variable, class, module, import, export
- Terminal: stdout, stderr, stdin, pipe, redirect
- API: endpoint, request, response, header, payload
- DevOps: deploy, build, CI/CD, container, image

## Mixed Phrasing Examples

- "Tôi đã tạo 3 file Python trong thư mục src/"
- "Lệnh `git push` bị lỗi — remote có commit mới hơn"
- "Bạn muốn tôi deploy lên staging hay production?"
- "API trả về status 404 — endpoint `/api/users` không tồn tại"

## Updating This Skill

To update Vietnamese conventions, run:
```
hermes skills edit vietnamese-language
```

Or ask Hermes: "Cập nhật skill tiếng Việt với quy tắc mới: ..."
