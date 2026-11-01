# yh-gl · 应化 Graph-Loop Skill

资源受限下的 AI 协同开发方法论，以 agent skill 形式分发。**整目录自包含**，拷到任何宿主即可运行，不依赖本仓库存在。

## 目录结构

```
yh-gl/
├── SKILL.md              # 路由层：agent 接到任务后的定级/升档/按需路由入口
└── references/           # 方法论正文（agent 按需读，人不通读）
    ├── 00-总导读.md       # 体系定位与接入索引
    ├── 01-v1-理念层-通用指南.md
    ├── 02-v2-机制层-实施手册.md
    ├── 03-v3-调度层-滚动交付手册.md
    └── README.md         # 新项目接入本方法论的步骤
```

分工：**SKILL.md 只做路由决策，不复制手册正文**；项目实例（L1 契约填空、模块路径映射、环境约束）写在各项目的规则文件里，不放本目录。

## 安装到宿主

把整个 `yh-gl/` 目录拷贝为宿主的 skill，例如 AtomCode：

```
~/.atomcode/skills/yh-gl/
```

外部工具（CBM / dao-distill / jev-router）均为可选增强，有则加速、无则降级，安装引导见 SKILL.md「工具预装引导」节。

## 发布 / 同步（维护者）

本仓库 `yh-gl/` 是**开发版**；skill 副本（如 `~/.atomcode/skills/yh-gl/`）是分发版。修改一律：

1. **先改仓库**，验证通过；
2. 再把 `yh-gl/` 整目录同步到 skill 副本（覆盖拷贝，勿只拷单个文件）。

**改版校对项**：SKILL.md 内引用的手册章节号（v2 §3.2/§3.3、v3 §2.7.1 等）须随手册改版核对，防止路由指向失效章节。

## 更多

- 方法论是什么、怎么在新项目启用 → [references/README.md](references/README.md)
- 体系全貌 → [references/00-总导读.md](references/00-总导读.md)
