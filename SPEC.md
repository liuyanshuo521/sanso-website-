# Sanso 品牌官网设计规范

## 1. Concept & Vision

Sanso 是一家追求极致体验的品牌，三位创始人刘颜硕（董事长）、杜创、张宇共同打造。网站整体风格参考 Apple 官网——极简、留白、大胆、现代。首页即展示三位核心人物，用大图、高质量排版和流畅动画传递品牌调性：简约而不简单，高级且有温度。

## 2. Design Language

### Aesthetic Direction
苹果式极简主义：大量留白、精致排版、微妙动效、功能至上。黑白灰为主色调，少量强调色点缀。

### Color Palette
```css
--bg-primary: #f5f5f7;       /* 苹果标志性浅灰背景 */
--bg-dark: #1d1d1f;           /* 深色区域 */
--text-primary: #1d1d1f;     /* 主文字 */
--text-secondary: #86868b;   /* 次要文字 */
--accent: #0071e3;           /* 苹果蓝 */
--white: #ffffff;
```

### Typography
- 标题：`SF Pro Display` 回退 `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- 正文：同 SF Pro Display
- 字重：标题 600-700，正文 400

### Spatial System
- 超大间距：section padding 120px+
- 内容最大宽度：1200px
- 图片比例：16:9 或 4:5 人像

### Motion Philosophy
- 入场动画：opacity 0→1, translateY 30px→0, 600ms ease-out
- 交错延迟：100-150ms per item
- 滚动触发：Intersection Observer
- 悬停：scale 1.02, 300ms ease

## 3. Layout & Structure

### Hero Section
- 全屏高度，背景渐变或纯色
- 品牌名 "Sanso" 大字居中
- 简短 tagline
- 向下滚动提示箭头

### Founders Section（三位创始人）
- 三列布局，每列一个人物卡片
- 大图 + 姓名 + 职位 + 一句话简介
- 卡片悬停有微妙阴影提升

### About Section
- 品牌故事/价值观
- 简洁的段落文字

### Footer
- 版权信息
- 社交链接图标

## 4. Features & Interactions

- **滚动动画**：元素进入视口时渐入
- **导航栏**：固定顶部，滚动时背景模糊
- **人物卡片**：悬停放大 + 阴影
- **平滑滚动**：锚点跳转使用 smooth scroll
- **响应式**：移动端单列堆叠

## 5. Component Inventory

### Navigation
- 透明背景，滚动后毛玻璃效果
- Logo 左对齐，导航项右对齐

### Founder Card
- 圆角图片（16px radius）
- 姓名：24px bold
- 职位：16px 次要色
- 简介：14px

### CTA Button
- 蓝色背景，白色文字
- 圆角 24px（全圆角风格）
- 悬停亮度提升

## 6. Technical Approach

单文件 HTML + CSS + Vanilla JS。纯前端实现，无需构建工具。