# 小火箭 · 求职工作台

产品策划方案的交互演示。所有岗位、公司、会话和个人资料均为虚构示例。

[打开小火箭在线 Demo](https://rocket-resume-demo-zhan820.lkhnj.chatgpt.site/)

以小火箭为主题的卡通求职工作台：奶油色背景、原创火箭角色、漫画描边、贴纸按钮和轨道式步骤导航。桌面端提供岗位列表与详情、会话列表与聊天窗口；手机端提供底部导航和独立岗位详情。

可以体验岗位搜索、来源与城市筛选、收藏、关键词匹配、招呼草稿编辑、会话消息、HR 索要简历后的逐次确认，以及附件快照预览。官网网申分为基本信息、教育经历、项目经历和附件四步，支持草稿保存、逐份确认、重复提交拦截与断网结果核验。投递记录关联对应岗位和本次使用的简历。

这是独立静态前端，未接入大模型、招聘平台或真实投递服务。匹配及文案使用本地规则；没有真实登录、文件上传、外发消息或后端存储。资料、草稿和记录保存在当前浏览器的 localStorage，刷新仍保留，可在“场景设置”重置。体验时请使用虚构资料。

实际实现为原生 JavaScript ES Modules、HTML、CSS 和 localStorage。源文件位于 `dist/`：`engine.mjs` 管理确认、版本和去重，`workspace.mjs` 管理会话与表单状态，`workspace-ui.mjs` 渲染界面，`workspace.css` 和 `cartoon.css` 定义布局与漫画主题。GitHub 镜像把 `dist/` 内容放在仓库根目录。无外部字体、CDN 或运行时依赖。

## 火箭插画

项目资产：`dist/assets/rocket-mascot.png`，由内置图像生成工具创作，透明背景原图随项目托管。

最终提示词：

> Use case: illustration-story. Asset type: original transparent mascot illustration used inside a Chinese job-search workspace app named 小火箭. Create one beautifully designed charming cartoon rocket mascot, angled diagonally ascending toward upper right, rounded cream-colored body, orange-red nose cone and fins, dark indigo thick clean ink contours, large round pale-blue porthole with a tiny friendly smiling face visible behind glass, yellow-orange flame and compact puffy cream exhaust. Surround it sparingly with 3 small hand-drawn four-point stars and one tiny ringed planet. Sophisticated contemporary editorial comic art, delightful vinyl-sticker shape language, subtle paper grain within flat color areas, carefully balanced anatomy, expressive bold hand-drawn curves, no 3D rendering. Palette coordinated for a cream UI: warm ivory #fffaf0, persimmon #f7774b, dark indigo #30304c, sky blue #b9d9f4, butter yellow #f5ce61. Isolated cutout on genuinely transparent background with alpha; complete silhouette with generous clear margin, no cropping, no text or letters, no UI screenshot, no border rectangle, no watermark. Composed to remain recognizable at 160px tall and also attractive as a hero illustration.

## 方案拟采用的技术

React / Electron 提供操作界面；Python / FastAPI 处理任务；文本解析、OCR 与大模型处理资料与文案；Playwright 负责浏览器执行；LangGraph 管理任务与确认；SQLite 保存记录。以上是规划技术栈，与此静态演示的实际实现区分。

BOSS 等平台接入需另外核验许可和实际页面适配，不能把本演示理解为已完成平台接入。
