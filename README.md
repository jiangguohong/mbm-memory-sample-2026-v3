# MBM Neuron-Memory Sample (2026-06) · v3 重建版

本仓库为 **v3 脱敏样本的删除重建版（fresh rebuild）**。原同名仓因 git 历史含未脱敏明文，已由用户裁定弃用并删除；本仓为**全新提交历史**，无任何历史明文残留，现以 public 发布。

## 数据
- **1,605 条**记忆记录，采集于 2026-06，来自 MBM（Metabolic Brain Memory）系统
- 层级分布：L0=79 / L1=91 / L2=139 / L3=831 / L4=58 / L5=139 / l1_raw=76 / l2_fact=114 / l4_identity=78
- 生成范围：`cube_id` 非空 且 `created_at` 落在 2026-06
- 文件：`sample_memory_2026-06.csv`（UTF-8，逗号分隔，含表头）

## 脱敏处置（v3）
- **凭证字段整条删除**：含 `sk-` / `ghp_` / `api_key` / `token` / 密钥 / 凭证 / 私钥 的记录共 **56** 条整条置 `[CREDENTIAL_REDACTED]`，无一明文残留。
- **身份档案整条红**：身份层（L0）及强身份词命中记录共 **225** 条整条置 `[PERSONAL_REDACTED]`。
- **商业指纹脱敏**：真实平台名 / 定价 / 副业活动 → `[BIZ]` / `[PRICE]`（**63** 条）。
- 本地路径（`C:/Users...`、`/Users/...`）、内部系统名（Hetu / 鸿巢 / OpenClaw / hy-memory 等）、端口、IP、邮箱、手机号、agent 名（含驼峰写法）、厂商英文名（SiliconFlow 等）全部清洗。
- 经独立 27 项泄露矩阵重检：**0 命中**。

## 列说明
| 列 | 含义 |
|---|---|
| sample_id | 顺序编号 |
| layer | L0/L1/L2/L3/L4/L5/l1_raw/l2_fact/l4_identity |
| content_len | 原始记忆字符长度 |
| excerpt_anon | 截断 + 脱敏后的摘录（含 `[...]` 占位符表示已抹除内容） |
| source_anon | `inst`（已匿名化来源） |

## 用途
与论文配套的脱敏样本，供可复现性验证。不含任何真实凭证、个人身份信息或内部标识。

## 备注
- 本仓为公开样本，**请勿将任何真实凭据或个人信息反向写入**。
- 如需引用，请使用本仓库公开链接。
