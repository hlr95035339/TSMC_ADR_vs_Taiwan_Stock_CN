# 台積電 ADR vs 台股價差分析

## 專案簡介
**為何台積電ADR長期相較台股存在溢價？此價差是否具有可交易性？** 透過分析台積電ADR (NYSE: TSM) 與台股(TWSE: 2330)之間的價格差異，並探討其成因與是否存在可行的交易策略。

---

## 核心發現（Key Insights）
- ADR 長期存在 **15%–25% 溢價**
- 價差具有**持續性（persistence）**，不易完全套利
- 價差受以下因素影響：
  - 匯率（USD/TWD）
  - 美股市場情緒（特別是科技股）
  - 市場流動性差異

---

## 數據來源（Data）
- 台股：台積電（2330）
- 美股：TSMC ADR（TSM）
- 匯率：USD/TWD

---

## 方法（Methodology）

### 價差定義（Spread）

---

> 註：1 ADR = 5 股台積電股票

---

## 分析內容（Analysis）
- 價格走勢比較（ADR vs 台股）
- 價差（Spread）時間序列分析
- 價差分布（Distribution）
- 滾動平均（Rolling Mean）
- Z-score 標準化分析

---

## 交易策略（Backtest）

基於 **均值回歸（Mean Reversion）** 假設，設計簡單交易策略：

### 策略邏輯：
- 當 Z-score > 2  
  → 做空 ADR / 做多台股（價差過高，預期回落）

- 當 Z-score < -2  
  → 做多 ADR / 做空台股（價差過低，預期回升）

---

## 回測結果（Backtesting Results）
- 累積報酬（Cumulative Return）
- 勝率（Win Rate）
- 最大回撤（Max Drawdown）

---

## 風險調整報酬（Sharpe Ratio）
---

### 解讀：
- 衡量「每單位風險帶來的報酬」
- Sharpe Ratio 越高，代表策略越穩定且有效

---

## 交易意涵（Trading Implications）
- 當價差偏離歷史區間時，可能存在均值回歸機會
- 可採用：
  - 做多低估市場
  - 做空高估市場

⚠️ 注意：
- ADR 與台股之間存在轉換限制
- 市場摩擦（交易成本、流動性）會影響套利效果

---

## 工具（Tools）
- Python（Pandas, NumPy）
- Matplotlib / Seaborn
- Time Series Analysis

---

## 專案價值（Project Value）
本專案展示從數據分析到投資策略的完整流程：
- 建立金融市場價差分析能力
- 設計與驗證交易策略
- 評估風險與報酬（Sharpe Ratio）

---

## 技能展示（Skills）
- 資料分析（EDA）
- 時間序列分析（Time Series）
- 交易策略設計（Backtesting）
- 風險評估（Sharpe Ratio）
- Python 數據分析
