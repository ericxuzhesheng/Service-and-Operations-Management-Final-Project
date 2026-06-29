# 服务与运营管理期末论文 | Service and Operations Management Final Project

<p align="center">
  <a href="#中文"><img src="https://img.shields.io/badge/语言-中文-E84D3D?style=for-the-badge&labelColor=3B3F47" alt="中文"></a>
  &nbsp;
  <a href="#english"><img src="https://img.shields.io/badge/Language-English-2F73C9?style=for-the-badge&labelColor=3B3F47" alt="English"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/LaTeX-XeLaTeX-008080?style=for-the-badge&logo=latex&logoColor=white" alt="LaTeX">
  <img src="https://img.shields.io/badge/案例-Grill%20Rite-4CAF50?style=for-the-badge" alt="Grill Rite Case">
  <img src="https://img.shields.io/badge/量化分析-风险池化·库存优化-9B51E0?style=for-the-badge" alt="Quantitative Analysis">
  <img src="https://img.shields.io/badge/License-MIT-F2C94C?style=for-the-badge" alt="MIT License">
</p>

---

## 中文

### 一句话概览

本项目是一篇面向**服务与运营管理**课程的期末研究论文，以 **Grill Rite** 电烤架公司的多仓库库存协调问题为案例，运用库存管理、风险池化、牛鞭效应等运营管理理论，结合量化数值分析，提出系统性改进方案。

**核心结论：** 通过引入正式的 $(Q,R)$ 库存策略、季节性需求预测与风险池化机制，Grill Rite 的库存相关总成本预计可降低约 **23%**（约 \$355{,}000/年），同时显著改善客户服务水平。

### 快速导航

| 你想看什么 | 入口 |
|---|---|
| 研究问题 | [研究问题](#研究问题) |
| 方法论概述 | [方法论](#方法论) |
| 量化分析结果 | [量化分析](#量化分析) |
| 改进建议 | [改进建议](#改进建议) |
| 如何编译 | [快速开始](#快速开始) |

---

### 研究问题

> Grill Rite 拥有稳定的生产能力和忠诚的员工队伍，但为什么其多仓库分销系统仍然面临频繁的缺货、库存上升和客户投诉？如何运用运营管理理论来诊断和改善这些问题？

本论文从三个层面展开分析：首先识别运营问题的根源，然后用库存理论和供应链协调框架来解释这些问题的成因，最后提出切实可行的改进方案，并通过量化估算来评估改进的潜在收益。

### 方法论

| 理论框架 | 应用 |
|---|---|
| 库存策略设计 $(Q, R)$ | 为各仓库设定基于数据驱动的再订货点与经济订货量 |
| 报童模型与季节性分析 | 量化季节性需求波动对库存积压和缺货的影响 |
| 风险池化与多级库存 | 利用中心化库存降低安全库存需求（$\sqrt{n}$ 法则） |
| 牛鞭效应 | 解释仓库间信息不对称和激励错位导致的订单波动放大 |
| 成本效益分析 | 估算当前系统与改进方案的年度库存总成本差异 |

### 量化分析

论文包含以下量化分析内容，所有参数均基于案例定性描述进行合理假设：

**季节性需求画像：** 电烤架产品的月需求指数（$I_m$）在旺季（5–7月）达到 1.40–1.60，淡季（11–2月）仅 0.40–0.60。在恒定产出策略下，季节性库存缓冲约为 10,420 单位，年持有成本约 \$520,000。

**$(Q,R)$ 策略参数：**

| 时期 | 周均需求 $\mu_w$ | 周标准差 $\sigma_w$ | 再订货点 $R$ | 安全库存 SS | 经济订货量 $Q^*$ |
|---|---:|---:|---:|---:|---:|
| 旺季 (5–7月) | 1,538 | 222 | 3,594 | 518 | 1,000 |
| 淡季 (11–2月) | 423 | 97 | 1,072 | 226 | 1,000 |

**风险池化效益：** 将三个区域仓库的安全库存集中到中央仓库，可将安全库存降低 **42%**，年节省约 \$98,500；混合模式（中央池化+区域缓冲）仍可节省 **27%**（约 \$63,200/年）。

**成本对比总览：**

| 成本项目 | 当前系统 | 改进方案 | 变化 |
|---|---:|---:|---|
| 安全库存持有成本 | \$580,000 | \$400,000 | -31% |
| 季节性缓冲持有成本 | \$520,000 | \$440,000 | -15% |
| 订货与设置成本 | \$125,000 | \$140,000 | +12% |
| 缺货与失销成本 | \$300,000 | \$150,000 | -50% |
| 横向调拨成本 | — | \$40,000 | 新增 |
| **合计** | **\$1,525,000** | **\$1,170,000** | **-23%** |

### 改进建议

论文提出五项系统性改进建议：

1. **设计正式库存策略** — 为每个仓库的每个 SKU 建立 $(Q,R)$ 或 $(P,T)$ 策略，安全库存与需求波动率和服务水平目标挂钩
2. **引入需求预测与 S&OP 流程** — 利用历史销售数据构建季节性指数，建立月度产销协调会议
3. **实现跨仓库库存池化** — 启用横向调拨机制，将中央仓库定位为风险池化缓冲节点
4. **重新对齐激励与绩效指标** — 从单仓考核转向系统级服务水平与总供应链成本指标
5. **逐步引入 WMS/DRP 技术** — 分阶段实施仓储管理系统和分销需求计划工具

### 论文结构

```text
.
├── paper/                           # 论文源文件
│   ├── main.tex                     # LaTeX 正文（XeLaTeX 编译）
│   ├── references.bib               # BibTeX 参考文献
│   └── OM_cover.pdf                 # 课程论文封面
├── materials/                       # 课程材料
│   ├── 01. Term Paper Requirement.pdf   # 作业要求
│   ├── 02. OM Cases.pdf                 # 案例材料
│   ├── 03. 课程论文封面模板.docx         # 封面模板
│   └── 04. Paper Grading Criteria.pdf   # 评分标准
├── README.md                        # 本文件
├── LICENSE                          # MIT 许可证
└── .gitignore                       # Git 忽略规则
```

### 快速开始

```bash
cd paper
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

### 参考文献

论文引用了以下核心文献：
- Stevenson, W.J. *Operations Management*, 13th ed. (2017)
- Cachon, G. & Terwiesch, C. *Matching Supply with Demand*, 4th ed. (2018)
- Lee, H.L. et al. "The Bullwhip Effect in Supply Chains" (1997)
- Simchi-Levi, D. et al. *Designing and Managing the Supply Chain*, 3rd ed. (2008)
- Eppen, G.D. "Effects of Centralization on Expected Safety-Stock Costs" (1979)
- Chopra, S. & Meindl, P. *Supply Chain Management*, 6th ed. (2016)
- Silver, E.A. et al. *Inventory Management and Production Planning and Control*, 3rd ed. (1998)

---

## English

### At A Glance

This repository contains a final term paper for a **Service and Operations Management** course. Using the **Grill Rite** electric barbecue grill company as a case study, it applies inventory management, risk pooling, and bullwhip effect theories to diagnose multi-warehouse coordination failures and propose data-driven solutions with quantitative analysis.

The main finding is that implementing formal $(Q,R)$ inventory policies, seasonal demand forecasting, and risk pooling mechanisms can reduce Grill Rite's total inventory-related costs by approximately **23%** (roughly \$355{,}000 annually) while significantly improving customer service levels.

### Navigation

| Looking for | Section |
|---|---|
| Research question | [Research Question](#research-question) |
| Methodology | [Methodology](#methodology) |
| Quantitative results | [Quantitative Analysis](#quantitative-analysis) |
| Recommendations | [Recommendations](#recommendations) |
| How to compile | [Quick Start](#quick-start) |

### Research Question

> Despite possessing stable production capacity and a loyal workforce, why does Grill Rite's multi-warehouse distribution system suffer from frequent stockouts, rising inventories, and increasing customer complaints? How can operations management theory diagnose and resolve these problems?

The paper analyzes the problem at three levels: identifying root operational causes, explaining them through inventory and supply chain coordination theory, and proposing actionable improvements with quantitative estimates of potential savings.

### Methodology

| Theoretical Framework | Application |
|---|---|
| Inventory policy design $(Q, R)$ | Data-driven reorder points and economic order quantities for each warehouse |
| Newsvendor model and seasonal analysis | Quantifying the impact of seasonal demand variability on inventory buildup and stockouts |
| Risk pooling and multi-echelon inventory | Reducing safety stock requirements through centralization ($\sqrt{n}$ rule) |
| Bullwhip effect | Explaining order variability amplification from information asymmetry and misaligned incentives |
| Cost-benefit analysis | Estimating the annual inventory cost difference between current and proposed systems |

### Quantitative Analysis

The paper includes the following quantitative analyses, with parameters derived from reasonable assumptions based on the qualitative case description:

**Seasonal demand profile:** Monthly demand indices ($I_m$) range from 0.40–0.60 in off-peak months (Nov–Feb) to 1.40–1.60 in peak months (May–Jul). Under constant output, the seasonal inventory buffer is approximately 10,420 units, costing about \$520,000 annually in carrying costs.

**$(Q,R)$ policy parameters:**

| Period | Weekly mean $\mu_w$ | Weekly std $\sigma_w$ | Reorder point $R$ | Safety stock SS | EOQ $Q^*$ |
|---|---:|---:|---:|---:|---:|
| Peak (May–Jul) | 1,538 | 222 | 3,594 | 518 | 1,000 |
| Off-peak (Nov–Feb) | 423 | 97 | 1,072 | 226 | 1,000 |

**Risk pooling benefit:** Centralizing safety stock from three regional warehouses at the central warehouse reduces safety stock by **42%**, saving approximately \$98,500/year. A hybrid approach (central pool + regional buffers) still saves **27%** (about \$63,200/year).

**Cost comparison:**

| Cost Component | Current | Proposed | Change |
|---|---:|---:|---|
| Safety stock holding | \$580,000 | \$400,000 | -31% |
| Seasonal buffer carrying | \$520,000 | \$440,000 | -15% |
| Ordering and setup | \$125,000 | \$140,000 | +12% |
| Stockout and lost sales | \$300,000 | \$150,000 | -50% |
| Lateral transshipment | — | \$40,000 | New |
| **Total** | **\$1,525,000** | **\$1,170,000** | **-23%** |

### Recommendations

The paper proposes five integrated recommendations:

1. **Design formal inventory policies** — Establish $(Q,R)$ or $(P,T)$ policies for every SKU at each warehouse, linking safety stock to demand variability and service level targets
2. **Introduce forecasting and S&OP** — Build seasonal indices from historical sales data and establish monthly Sales & Operations Planning meetings
3. **Enable cross-warehouse inventory pooling** — Implement lateral transshipment mechanisms and reposition the central warehouse as a risk-pooling buffer node
4. **Realign incentives and metrics** — Shift from local warehouse KPIs to system-wide service level and total supply chain cost metrics
5. **Gradual WMS/DRP adoption** — Phase in Warehouse Management Systems and Distribution Requirements Planning tools

### Repository Structure

```text
.
├── paper/                           # Paper source files
│   ├── main.tex                     # LaTeX source (compile with XeLaTeX)
│   ├── references.bib               # BibTeX bibliography
│   └── OM_cover.pdf                 # Course paper cover page
├── materials/                       # Course materials
│   ├── 01. Term Paper Requirement.pdf   # Assignment requirements
│   ├── 02. OM Cases.pdf                 # Case study materials
│   ├── 03. 课程论文封面模板.docx         # Cover page template
│   └── 04. Paper Grading Criteria.pdf   # Grading rubric
├── README.md                        # This file
├── LICENSE                          # MIT License
└── .gitignore                       # Git ignore rules
```

### Quick Start

```bash
cd paper
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

### References

- Stevenson, W.J. *Operations Management*, 13th ed. (2017)
- Cachon, G. & Terwiesch, C. *Matching Supply with Demand*, 4th ed. (2018)
- Lee, H.L. et al. "The Bullwhip Effect in Supply Chains" (1997)
- Simchi-Levi, D. et al. *Designing and Managing the Supply Chain*, 3rd ed. (2008)
- Eppen, G.D. "Effects of Centralization on Expected Safety-Stock Costs" (1979)
- Chopra, S. & Meindl, P. *Supply Chain Management*, 6th ed. (2016)
- Silver, E.A. et al. *Inventory Management and Production Planning and Control*, 3rd ed. (1998)

---

## License

MIT License. See [LICENSE](LICENSE) for details.
