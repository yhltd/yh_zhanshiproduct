# 视觉升级计划：商务深蓝 & 科技感调色盘

## 1. 核心色彩定义
将目前的 `slate` (深灰) 体系升级为商务科技风格：
- **主色 (Primary)**: `#001f3f` (商务深蓝) $\rightarrow$ 用于导航栏、Logo、关键按钮、激活状态、页眉遮罩。
- **辅助色 (Accent)**: Tech Blue)**: `#007BFF` 或 `indigo-600` $\rightarrow$ 用于强调色、搜索框聚焦、链接、进度条。
- **点缀色 (Highlight: Tech Gold)**: `#D4AF37` 或 `amber-400` $\rightarrow$ 用于特殊标记、高光效果。
- **背景色 (Background)**: `#fcfcfd` $\rightarrow$ 保持极简白/浅蓝灰，增加深度感。
- **文字色 (Text)**: `slate-900` $\rightarrow$ `slate-900` (标题) / `slate-600` (正文)。

## 2. 具体修改方案

### A. 全局样式与背景 (CSS/HTML)
- **Body**: 将 `business-bg` 的渐变从 `slate-50 -> blue-50` 调整为 `slate-50 -> blue-100/30`。
- **Decorative Blobs**: 将 `bg-indigo-200` 和 `bg-slate-200` 调整为 `bg-blue-200` 和 `bg-indigo-100`，增强蓝色调统一性。

### B. 导航栏与头部 (Nav & Header)
- **Logo**: `bg-slate-900` $\rightarrow$ `bg-[#001f3f]`。
- **文字**: `text-slate-900` $\rightarrow$ `text-[#001f3f]`。
- **Hero Overlay**: `rgba(15, 23, 42, 0.85)` $\rightarrow$ `rgba(0, 31, 63, 0.85)` (深蓝渐变遮罩)。
- **Hero Text**: 保持白色，但将辅助文本 `text-slate-300` 略微调亮。

### C. 交互组件 (Components)
- **搜索框**: 
    - `focus:ring-indigo-500/10` $\rightarrow$ `focus:ring-blue-500/20`。
    - `focus:border-indigo-600` $\rightarrow$ `focus:border-[#001f3f]`。
- **分类标签 (Category Pill)**:
    - 激活状态: `bg-slate-900` $\rightarrow$ `bg-[#001f3f]`，`border-slate-900` $\rightarrow$ `border-[#001f3f]`。
    - 悬停状态: `hover:border-slate-900` $\rightarrow$ `hover:border-[#001f3f]`。
- **视频卡片 (Video Card)**:
    - 标题悬停: `group-hover:text-indigo-600` $\rightarrow$ `group-hover:text-blue-600`。
    - 标签: `bg-slate-900/80` $\rightarrow$ `bg-[#001f3f]/80`。
- **分页按钮**: 
    - 激活状态: `bg-slate-900` $\rightarrow$ `bg-[#001f3f]`。

### D. 模态框 (Modals)
- **验证模态框**:
    - 按钮: `bg-slate-900` $\rightarrow$ `bg-[#001f3f]`。
    - 图标背景: `bg-slate-100` $\rightarrow$ `bg-blue-50`。

## 3. 实施步骤
1. 修改 `<style>` 块中的颜色变量和渐变定义。
2. 替换 HTML 标签中的 Tailwind 颜色类 (例如 `bg-slate-900` $\rightarrow$ `bg-[#001f3f]`)。
3. 更新 JavaScript 中动态生成的 HTML 字符串（分类标签、产品卡片、分页）。
