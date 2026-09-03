# Relay Monitor Author

[![npm version](https://img.shields.io/npm/v/relay-dsh-plugin-monitor-author?label=npm)](https://www.npmjs.com/package/relay-dsh-plugin-monitor-author)
[![CI](https://github.com/yangbobo2021/relay-dsh-plugin-monitor-author/actions/workflows/ci.yml/badge.svg)](https://github.com/yangbobo2021/relay-dsh-plugin-monitor-author/actions/workflows/ci.yml)
[![MIT license](https://img.shields.io/github/license/yangbobo2021/relay-dsh-plugin-monitor-author)](LICENSE)

English | [中文](README.zh.md)

DeepSeek Harness plugin that contributes the `relay-monitor-author` Skill to DSH's
native Skill catalog. The Skill guides the current DSH Agent through live Monitor
Bundle discovery, plugin preference, least-authority custom authoring, validation,
and durable installation.

Install the exact public release together with Monitor Core:

```bash
npx @deepseek-ai/dsh@0.1.2-rc.1 plugin --profile web add --save-exact \
  relay-dsh-plugin-monitors@0.3.2-rc.1 \
  relay-dsh-plugin-monitor-author@0.1.2-rc.1
```

The same artifact retains compatibility with audited DSH `0.1.2-alpha.3` profiles.

Install this package together with `relay-dsh-plugin-monitors`. DSH users can ask
the Agent to wait for an external condition, load the Skill through DSH's native
Skill UI/tool, or invoke `/relay-monitor-author` explicitly. The Skill uses the
Monitor tools already scoped to the current DSH root Session; it does not create a
Codex plugin and does not bypass Relay authorization.

Unloading this plugin removes the Skill from new DSH catalog observations. It does
not stop or rewrite Monitors that were already committed by Monitor Core.

See [SPEC.md](SPEC.md) and [docs/acceptance-scenarios.md](docs/acceptance-scenarios.md).
