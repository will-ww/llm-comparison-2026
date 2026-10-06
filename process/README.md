# 工作过程记录

本目录以 issue 形式记录项目的完整工作过程，编号即时间顺序：

| # | 阶段 | 核心产出 | 关键技术点 |
|---|---|---|---|
| 01 | [深度研究](issue-01-深度研究.md) | 研究报告 | 多源交叉验证、口径分离 |
| 02 | [PPT 初版](issue-02-PPT初版.md) | 14 页 PPT | PPTD DSL、ECharts 无头渲染管线 |
| 03 | [PPT 改版](issue-03-PPT改版.md) | 21 页峰会版 | 数据源切换、三类受众适配 |
| 04 | [翻页视频](issue-04-翻页视频.md) | 67s 无声版 | FFmpeg xfade 时间轴公式 |
| 05 | [研究视频](issue-05-研究视频.md) | 10 分钟配音版 | TTS 逐页配音、不等长 xfade 链音画对齐 |
| 06 | [封面物料](issue-06-封面物料.md) | 封面图 + 发布文案 | 视觉体系延续、移动端可读性 |

## 工具链总览

```
Deep Research（多轮检索+交叉验证）
    └─→ kimi-slides（PPTD YAML DSL → 校验 → 可编辑源文件 → pptx）
          ├─ ECharts → Chromium 无头渲染 → PNG 图表
          └─→ 逐页 PNG → FFmpeg xfade → 翻页视频
                └─ + TTS 逐页配音 + AI 配乐 → 10 分钟研究视频
                      └─ kimi-design → B 站封面
```

全程由 Kimi（Moonshot AI）执行，人类负责需求澄清、数据口径确认（咨询版报告）与最终验收。
