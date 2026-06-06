# HTML PPT Collection

> 四个顶级的 HTML PPT 生成工具 + GSAP 动画引擎，一站式合集。做 PPT 时从这里挑，不用再到处找。

## 合集速览

| 项目 | Stars | 许可证 | 核心亮点 | 适用场景 |
|------|-------|--------|---------|---------|
| [html-ppt-skill](./html-ppt-skill/) | 5.6k | MIT | 36 主题、31 布局、47 动画、演讲者模式 | 全能型，主题和布局最丰富 |
| [frontend-slides](./frontend-slides/) | 20.5k | MIT | 34 粗体模板、PPTX 转换、视觉风格发现 | 从 PPTX 转换、粗体设计风格 |
| [guizang-ppt-skill](./guizang-ppt-skill/) | 15.3k | AGPL-3.0 | 电子杂志风 + 瑞士国际主义风、配图生成 | 个人风格强烈的演讲、发布会 |
| [huashu-design](./huashu-design/) | 16.5k | MIT | 40 种设计风格、可编辑 PPTX 导出、视频/GIF 导出 | 全流程设计交付（原型→PPT→视频） |
| [GSAP](./GSAP/) | 25.6k | Standard | 高性能 JS 动画引擎，ScrollTrigger 等插件 | 为以上 PPT 工具添加高级动画 |

---

## 如何选择

### 按需求选

| 你的需求 | 推荐工具 | 理由 |
|---------|---------|------|
| 主题多、布局全、随手做 PPT | **html-ppt-skill** | 36 主题 + 31 布局，覆盖面最广 |
| 从已有 PPTX 转 HTML | **frontend-slides** | 内置 PPTX 提取脚本 |
| 要粗体/杂志风格 | **frontend-slides** | 34 个粗体设计模板 |
| 演讲/发布会、强个人风格 | **guizang-ppt-skill** | 电子杂志 + 瑞士风，叙事感强 |
| 需要导出可编辑 PPTX | **huashu-design** | 唯一支持导出可编辑 PPTX |
| 需要做 App/Web 原型 | **huashu-design** | 支持交互原型 + iPhone 框 |
| 需要视频/GIF 导出 | **huashu-design** | 完整视频导出工具链 |
| 想加高级动画效果 | **GSAP** | 搭配以上任一工具使用 |

### 按风格选

| 风格 | 工具 |
|------|------|
| 商务/专业 | html-ppt-skill（多套商务主题）、frontend-slides（Blue Professional） |
| 科技/极客 | html-ppt-skill（Cyber Terminal）、guizang-ppt-skill（瑞士风）、frontend-slides（Terminal Green） |
| 杂志/编辑 | guizang-ppt-skill（Style A 电子杂志风）、frontend-slides（Vintage Editorial） |
| 创意/大胆 | frontend-slides（Bold Poster、Neo Grid）、huashu-design（40 种风格库） |
| 小红书/社交媒体 | html-ppt-skill（小红书白底/马卡龙）、guizang-ppt-skill（多平台封面） |

---

## 详细对比

### html-ppt-skill
- **作者**: lewislulu
- **定位**: 全能 HTML PPT Studio
- **主题**: 36 个 CSS 主题
- **布局**: 31 种单页布局（封面→目录→图表→感谢页全覆盖）
- **动画**: 27 CSS + 20 Canvas FX
- **特色**: 🎤 演讲者模式（S 键），含逐字稿 + 计时器
- **模板**: 15 个完整演示（融资、产品发布、技术分享、周报等）
- **安装**: `npx skills add lewislulu/html-ppt-skill`

### frontend-slides
- **作者**: zarazhangrui
- **定位**: 设计感优先的 HTML 幻灯片
- **模板**: 34 个粗体设计模板（Bold Template Pack）
- **风格预设**: 12 个精选视觉预设
- **转换**: 支持 PPTX → HTML 转换
- **部署**: 内置 Vercel 部署 + PDF 导出
- **特色**: 视觉风格发现（看图选风格，不用文字描述）
- **安装**: Claude Code 插件 / 直接使用 SKILL.md

### guizang-ppt-skill
- **作者**: op7418（归藏）
- **定位**: 强个人风格的网页 PPT
- **风格**: Style A（电子杂志风，5 主题 × 10 布局） + Style B（瑞士国际主义，4 锚点色 × 22 锁定版式）
- **配图**: 内置 GPT-Image 配图提示词模板
- **封面**: 多平台封面生成（公众号、小红书、视频号）
- **不适合**: 大段表格数据、培训课件
- **安装**: `npx skills add op7418/guizang-ppt-skill --skill guizang-ppt-skill`

### huashu-design
- **作者**: alchaincyf（桦树）
- **定位**: 全流程设计交付工具
- **风格库**: 40 种 HTML 原生风格（网页 20 + PPT 20）
- **交付物**: HTML 原型、可编辑 PPTX、MP4 视频、GIF、PDF
- **动画引擎**: 自研 Stage + Sprite + Easing 引擎
- **特色**: 5 维度设计评审、设备框架（iPhone/Android/macOS）
- **导出**: HTML→MP4→GIF 完整工具链

---

## GSAP 动画引擎

GSAP（GreenSock Animation Platform）是业界最强的 JS 动画库，可以作为以上四个 PPT 工具的动画增强层：

- **零依赖**，纯 JS，兼容所有主流浏览器
- **ScrollTrigger**：滚动驱动的动画
- **高性能**：比 jQuery 快 20 倍
- **用法示例**：

```html
<!-- CDN 引入 -->
<script src="https://cdn.jsdelivr.net/npm/gsap@3/dist/gsap.min.js"></script>
<script>
  // 基础动画
  gsap.from(".slide-title", { opacity: 0, y: 50, duration: 1 });
  gsap.to(".chart-bar", { scaleY: 1, duration: 0.8, stagger: 0.1 });
</script>
```

> 本仓库以 **git submodule** 方式引入 GSAP，指向官方仓库。克隆时加 `--recursive`：
> ```bash
> git clone --recursive https://github.com/chenp0401/ppt-toolkit.git
> ```

---

## 使用方式

### 在 AI Agent 中使用

各工具都提供了 `SKILL.md`，可直接被 Claude Code、Codex、Cursor 等 Agent 加载：

```bash
# 示例：安装 guizang-ppt-skill
npx skills add op7418/guizang-ppt-skill --skill guizang-ppt-skill

# 然后在对话中说
"帮我把这篇文章做成瑞士风 PPT，7 页左右"
```

### 直接使用模板文件

每个工具的 `templates/` 或 `assets/` 目录下都有可直接打开的 HTML 文件，浏览器打开即可预览所有主题和布局。

---

## 许可证

| 项目 | 许可证 | 商用 |
|------|--------|------|
| html-ppt-skill | MIT | ✅ 免费 |
| frontend-slides | MIT | ✅ 免费 |
| guizang-ppt-skill | AGPL-3.0 | ⚠️ 需遵守 AGPL |
| huashu-design | MIT | ✅ 免费 |
| GSAP | Standard | ✅ 免费（需保留版权声明） |

---

## 更新上游

各子项目会持续更新，定期同步：

```bash
# 更新 GSAP submodule
git submodule update --remote GSAP

# 更新其他四个（直接拷贝的代码，需手动同步）
# 建议关注原仓库的 Release 页面
```

---

## 致谢

感谢以下优秀项目及其作者：

- [lewislulu/html-ppt-skill](https://github.com/lewislulu/html-ppt-skill)
- [zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides)
- [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)
- [alchaincyf/huashu-design](https://github.com/alchaincyf/huashu-design)
- [greensock/GSAP](https://github.com/greensock/GSAP)
