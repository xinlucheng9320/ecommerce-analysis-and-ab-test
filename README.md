# 电商用户行为分析与购买预测 / 手游A/B实验分析

## 项目概览
两个数据分析项目，覆盖SQL分析、RFM用户分层、机器学习建模、A/B实验统计检验全流程。

## 项目一：电商用户行为分析与购买预测
`project1_ecommerce_analysis.ipynb`

**数据来源**：[eCommerce Events History in Cosmetics Shop](https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop)（Kaggle，500万条）

**主要内容**：
- 数据清洗：处理40%缺失品牌字段、异常价格，存入SQLite
- 漏斗分析：发现浏览→购买整体转化率仅6.64%
- RFM用户分层：将2.5万购买用户分为高/中/低价值及流失风险四类
- 时段分析：识别10-12点及19点双高峰
- 购买预测：XGBoost表现最优（AUC=0.9643），加购次数为最强预测信号

**技术栈**：Python / SQL / scikit-learn / XGBoost / Tableau

---

## 项目二：手游留存策略A/B实验分析
`project2_ab_test.ipynb`

**数据来源**：[Mobile Games AB Testing Cookie Cats](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)（Kaggle，9万用户）

**主要内容**：
- SRM检验：验证随机分组有效性
- 卡方检验：次日留存差异不显著（p=0.076），七日留存差异显著（p=0.0016）
- 结论：关卡门设在第30关显著更优，建议保留现有方案

**技术栈**：Python / scipy / 假设检验

---

## 环境依赖
```
pandas / numpy / matplotlib / scipy / scikit-learn / xgboost / sqlite3
```

## Tableau看板
https://public.tableau.com/views/_17731416846920/1
