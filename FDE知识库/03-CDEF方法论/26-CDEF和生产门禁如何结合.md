# CDEF 和生产门禁如何结合

CDEF 给 FDE 项目提供推进路径，生产门禁给项目提供阶段判断。

一个解决“怎么走”，一个解决“什么时候能进入下一步”。如果只有 CDEF，项目可能推进得很快但证据不足；如果只有门禁，项目可能变成僵硬审批。两者结合，FDE 才能既灵活又可控。

从定义上看，CDEF 是方法论闭环，生产门禁是阶段性质量控制机制。CDEF 负责从 Context、Design、Engineer 到 Feedback 推进问题，门禁负责在关键节点检查证据、Owner、风险和回滚。

> **一句可以带走的判断：CDEF 让项目往前走，门禁让项目知道什么时候该停下来补证据。**

## CDEF 对应哪些门禁

| CDEF 阶段 | 对应门禁 | 核心判断 |
| --- | --- | --- |
| Context | Problem Confirmed | 真实问题是否被定义清楚 |
| Design | Prototype Ready | 是否切出可验证价值闭环 |
| Engineer 早期 | Prototype Exit | Demo 是否验证关键假设 |
| Engineer 中期 | Pilot Ready | 是否能进入有限真实场景 |
| Engineer 后期 | Production Ready | 是否具备生产运行条件 |
| Feedback | Handover Ready | 客户是否能接管并继续演进 |

这样一来，CDEF 不只是四个阶段，而是一条带门禁的交付链。

## 每个门禁要看什么

| 门禁 | 必须有的证据 |
| --- | --- |
| Problem Confirmed | 事实约束表、问题模型、业务损失 |
| Prototype Ready | 需求切片画布、验收标准、风险边界 |
| Prototype Exit | Demo 结果、用户反馈、未验证风险 |
| Pilot Ready | 真实用户、数据授权、人工兜底 |
| Production Ready | 评测、权限、监控、回滚、SLO |
| Handover Ready | 接管清单、运行手册、演练记录 |

门禁不是为了阻拦项目，而是为了避免项目带着隐性风险继续扩大。

## 一个贯穿例子

客户希望做“合同审查 AI”。

| 阶段 | 动作 | 门禁 |
| --- | --- | --- |
| Context | 发现真正痛点是法务初审耗时和风险条款遗漏 | Problem Confirmed |
| Design | 切出“采购合同付款条款审查” | Prototype Ready |
| Engineer | 用历史合同和规则库做 Demo | Prototype Exit |
| Engineer | 让 3 名法务在真实合同上试点 | Pilot Ready |
| Engineer | 接入权限、审计、评测和回滚 | Production Ready |
| Feedback | 把高频条款风险沉淀为产品模板 | Handover Ready |

这个过程里，CDEF 保持方向，门禁控制风险。

## 门禁不是一次性审批

FDE 项目里，门禁应该是工作方式的一部分。

每次进入下一阶段前，团队都要问：

- 这一阶段验证了什么？
- 还缺哪些证据？
- 谁负责下一阶段结果？
- 失败后怎么退回？
- 哪些经验要沉淀？

如果这些问题说不清，项目就不是不能继续，而是应该先补证据。

## 最小门禁矩阵

| 阶段 | 进入条件 | 退出标准 |
| --- | --- | --- |
| Context | 有业务 Sponsor 和初始问题 | 真实问题、约束和价值损失被记录 |
| Design | 问题模型已形成 | 价值切片、方案取舍和验收标准明确 |
| Engineer | 切片可验证 | Demo、试点、生产证据逐步补齐 |
| Feedback | 系统进入真实使用 | 指标复盘、客户接管、产品反哺完成 |

CDEF 和生产门禁结合后，FDE 项目就不再依赖个人英雄主义。

它变成一套可复查、可教学、可复制的交付方法。这一点，可能比单个项目成功更重要。
