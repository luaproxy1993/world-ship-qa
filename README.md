# 包装发布与质检（world-ship-qa）

在玩通 sitting 之后做独立世界包校验、加载门、资源全量抽查、游客冷启动路径、参考壳对等门和版本发布清单。

内容能玩，还不等于能发。本 skill 是发布门：校验包的自立与路径，不发明第二种打包格式，也不代替战役试玩门。

```text
/world-ship-qa
/world-ship-qa preflight | pack | loading | audit | guest | release | accept
```

## 安装

```bash
npx skills add luaproxy1993/world-ship-qa -y
```

或把本仓库拷到 `~/.grok/skills/world-ship-qa/`。

## 它做什么

试玩门已过之后，按清单跑：

1. 包校验（清单、相对路径、自包含，无密钥 / `.env` / 本机绝对路径）
2. 加载门（板先盖住，静帧 / 入场片解码后再交手）
3. 资源全量抽查（无断链、无失败片、无密钥、无源书原文）
4. 游客冷启动实测
5. 参考壳对等（对 doki-mesh-world：路径能过但壳更薄，不算通过）
6. 版本与发布清单

打包与 SDK 仍由原技能负责：`/doki-game-maker`、`/dokiimport`、`/rpg-campaign-maker`。本 skill 在它们之后跑，或指出它们还没跑。

## 相关仓库

- [doki-game-maker](https://github.com/luaproxy1993/doki-game-maker) — 卡带形状、导出静态树、无密钥 handoff
- [rpg-campaign-maker](https://github.com/luaproxy1993/rpg-campaign-maker) — 静态战役 `dist/` 与试玩门
- [mesh-rpg-craft](https://github.com/luaproxy1993/mesh-rpg-craft) — 网状战役锁序；出包前的制作层
- [world-bible](https://github.com/luaproxy1993/world-bible) / [world-bible-pack](https://github.com/luaproxy1993/world-bible-pack) — 世界书与美术包

## License

Skill text and scripts: use and modify. Do not ship other people's campaign books, official-book extracts, or secrets (API keys, `.env`, session files) in packs.
