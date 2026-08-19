# 蚂蚁阿福 × LibTV：AI 产品架构逆向分析

本交付基于两款产品在 2026-08-19 的真实页面取证，重点回答 Agent/工作流形态、技术流、功能等价 System Prompt 和完整 AI 产品架构。

原始页面取证：[蚂蚁阿福](https://github.com/turetegeblocfaun-star/antafu-product-teardown)；[LibTV](https://github.com/turetegeblocfaun-star/libtv-product-teardown)。

## 核心判断

- **蚂蚁阿福**：【合理推断】单一可见健康 Agent + 四类任务工作流 + 搜索/PDF/视觉工具；内部多 Agent【未知】。
- **LibTV**：【已确认】存在 LibTV Agent；【合理推断】单一可见创作 Agent + Skill 工作流 + 图片/视频模型与项目工具；内部多 Agent【未知】。
- 两款产品都不是纯固定工作流，也没有足够证据判定为多 Agent。

## 阅读顺序

1. `00-证据范围与结论口径.md`
2. `01-分析结果/01-双产品-Agent契约与技术流.md`
3. `02-提示词/02-蚂蚁阿福-功能等价SystemPrompt.md`
4. `02-提示词/03-LibTV-功能等价SystemPrompt.md`
5. `01-分析结果/04-双产品-产品全景架构-证据分层版.html`

## 重要声明

- 功能等价 System Prompt 用于复现可观察行为，不是官方隐藏提示词。
- “深度思考”“Skill”“模型”不是多 Agent 的直接证据。
- To-Be 中的 Supervisor/Worker/Reviewer 属于【建议设计】，不代表当前产品现状。
- 报告不包含账号凭证、临时二维码、真实医疗资料或隐藏模型信息。
