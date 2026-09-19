# Data format / 数据格式

Schema version: 1. UTF-8 JSON array at [data/prompts.json](data/prompts.json).

| Field | Meaning / 含义 |
| --- | --- |
| id | Stable MuseSignal item ID; shared across repositories / 稳定案例 ID |
| prompt | Complete original text / 完整原文 |
| category | Stable use-case key / 场景 key |
| model_key, model_name | Original model attribution / 原模型标签 |
| model_family | Distribution family; versions share a repository / 系列归属 |
| images | Original Twitter media URLs; may be empty / Twitter 原图，可为空 |
| author, source_url | Creator and original post / 作者与原帖 |
| musesignal_url, musesignal_url_zh | English / Chinese detail page |
| content_hash | SHA-256 of the canonical record excluding content_hash |
| license | null means no individual license verified / 未核实逐条许可 |

Deduplicate by id when combining datasets. A family dataset is a subset of the main catalog. Counts do not add across overlapping repositories. External images can become unavailable.

合并数据时按 id 去重。模型专题是总库子集，不能相加当作独立数量。图片外链可能失效。原模型标签不代表我们跨模型复测过效果。
