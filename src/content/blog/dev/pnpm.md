---
title: '不如 bun 吧'
publishDate: '2026-05-15'
updatedDate: '2026-05-15'
description: '使用 pnpm 时遇到的一些问题。'
language: '简体中文'
---

首先是在部署这篇博客时，原作者使用 `bun` 作为包管理器，`bun` 是允许幽灵依赖的。
而 `pnpm` 不允许，这就导致我在使用 `pnpm` 部署时产生了很多依赖缺失。
不过这个问题某种程度上来说也是原作者的问题就是了，其实不应该使用幽灵依赖的。

接着是在安装 `omniroute` 时，`pnpm` 无法正确运行 postinstall 脚本，
导致 `better-sqlite3` 原生模块无法构建而运行失败。
不过 `bun` 似乎也有这个问题，目前只推荐通过 `npm` 安装，
或者干脆使用 electron 版本。
