# 品牌电商销售数据看板

一个轻量、零构建的销售数据可视化看板。用一个 HTML 文件 + Chart.js，覆盖三年（或任意区间）的电商销售数据多维度展示。

## 在线访问

**GitHub Pages（推荐，启用后获得固定可分享链接）：**

> https://zzf-love.github.io/E-commerce-data-statistics-table/

启用方法（一次性，约 1 分钟生效）：
1. 打开仓库 → **Settings** → 左侧 **Pages**
2. **Source** 选 `Deploy from a branch`
3. **Branch** 选当前分支（`claude/eloquent-rubin-Nh2mC`）或合并到 `main` 后选 `main`，目录选 `/ (root)`
4. 保存，等 1 分钟刷新即可访问

**临时预览（无需任何配置）：**

> https://htmlpreview.github.io/?https://github.com/zzf-love/E-commerce-data-statistics-table/blob/claude/eloquent-rubin-Nh2mC/index.html

## 功能

- **7 张图表**：销售额趋势、同比 YoY、环比 MoM、年度同月对比、净销售 vs 推广费用、ROI（投产比）、推广费用占比饼图
- **时间维度切换**：全部 / 2025 / 2024 / 2023 / 最近 12 个月
- **数据管理抽屉**：直接在网页里编辑表格、增删行
- **导入数据**：支持 CSV 文件导入、从 Excel 直接复制粘贴
- **导出 CSV**：带同比、环比、ROI 计算列
- **本地持久化**：数据存到浏览器 `localStorage`，刷新不丢
- **响应式**：桌面、平板、手机三档断点

## 使用

1. 打开页面，默认是示例数据（2023–2025 三年）
2. 点右上角 **⚙ 数据管理** 打开抽屉
3. 直接改单元格、新增行；或点 **📋 从 Excel 粘贴** 把表格 4 列（月份、销售额、净销售额、推广费用）粘进去
4. 点 **保存并应用**，图表自动刷新
5. 点 **⬇ 导出 CSV** 一键导出

月份格式支持：`2025/01`、`2025-1`、`2025年1月` 等。

## 本地运行

无需任何构建工具，双击 `index.html` 即可。或：

```bash
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 技术栈

- 单文件 HTML / CSS / JS
- [Chart.js 4.4.1](https://www.chartjs.org/)（通过 CDN 引入）
- 浏览器 `localStorage` 存数据
