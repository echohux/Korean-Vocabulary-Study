# 实现核查 · Korean-Vocabulary-Study

以下结论来自当前仓库代码；ZIP 项目按归档内文件核查。代码中存在实现不代表线上端到端测试已通过。

| 说明范围 | 依据 | 核查结论 |
| --- | --- | --- |
| 调度 | [srs.ts](../src/services/srs.ts) | scheduleNext：good 首次 1 天，第二次 6 天；again 间隔 0 |
| 复习会话 | [review/index.tsx](../src/pages/review/index.tsx) | 基于 initialRecords 创建固定 queue；评分后 index 加一 |
| 例句 | [ExplanationPanel](../src/components/ExplanationPanel/index.tsx) | 读取 EXAMPLES、GRAMMAR_ZH，不调用模型 |
| 统计 | [analytics/index.tsx](../src/pages/analytics/index.tsx) | 记忆曲线由平均间隔经指数公式估算 |

## 评测状态

`EVALUATION.md` 是本次新增的待执行手动验收方案。仓库没有因此自动具备 Case 平台、模型评测、自动修复或线上监控；未执行用例不能填为通过。
