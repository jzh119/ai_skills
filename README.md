# Vocab HTML Builder v2 — 英文生词一键变互动学习页面

## 🎯 一句话介绍

> 输入任何包含英文生词的文件（Excel / Word / PDF / TXT / CSV），自动生成带**神经网络男女声对话朗读**的交互式 HTML 词汇学习页面，电脑手机都能用。

## ✨ 核心亮点

1. **任意格式输入** — xlsx / csv / txt / pdf / docx 通吃，丢进去就出结果
2. **AI 上下文感知对话** — 自动分析文档主题，生成贴合原始素材场景的对话，不是生硬模板
3. **神经网络音频** — Microsoft edge-tts 免费生成男女声 MP3，自然流畅不像机器音
4. **纯离线使用** — 中文翻译 + 音频全部嵌入，零网络依赖
5. **手机端完美运行** — 红米自带浏览器全功能正常，其他浏览器可装 HttpServer 解决
6. **蓝本级输出质量** — HTML 格式参照 `business_english_study_guide.html`（商务英语360项目实战验证）

## 📸 输出效果

生成的 HTML 包含：

```
📚 [主题] · 单词学习指南
├── 🔝 顶部导航（词数统计 + 分组标签 + 复习组入口）
├── 📇 单词卡片 × N
│   ├── 编号 + 单词 🔊 + 英/美音标 + 📝 复习按钮
│   ├── 📖 中文释义 + 词性
│   ├── 🌱 词根词缀
│   └── 💬 场景对话（3轮A/B/A，点击"中"看中文翻译）
├── 🔊 男声(GuyNeural) + 女声(JennyNeural) 朗读
└── 📝 localStorage 复习系统
```

## 🚀 使用方式

1. 把这个 skill 安装到 WorkBuddy
2. 对 AI 说：「帮我把 [文件名] 生成为词汇学习 HTML」
3. AI 自动执行 6 步流水线：
   - 读取文件 → 理解主题 → 提取生词 → 生成对话 → 构建HTML → 生成音频
4. 拿到 `output/` 文件夹，里面有 HTML + `audio/` 音频
5. 拷贝到手机/电脑同一目录，打开 HTML 即可

## 📦 包含内容

```
vocab-html-builder/
├── SKILL.md                        # 完整工作流文档
├── scripts/
│   ├── extract_words.py            # 5种格式单词提取器
│   ├── build_vocab.py              # HTML 构建引擎
│   ├── gen_dialogue_audio.py       # 对话音频生成（edge-tts）
│   └── gen_word_audio.py           # 单词音频生成（edge-tts）
└── assets/
    └── html-template.html          # 蓝本格式 HTML 模板
```

## 🔧 依赖

```bash
pip install pandas openpyxl edge-tts
pip install pdfplumber    # 仅 PDF 输入需要
pip install python-docx   # 仅 Word 输入需要
```

## 🎓 适用场景

- 商务英语学习（已验证 457 词项目）
- 考研/托福/雅思词汇复习
- 技术文档专业术语学习
- 任何英文教材/报告的生词整理

## 📱 手机端兼容性

| 浏览器 | 可用性 |
|--------|--------|
| 红米自带浏览器 | ✅ 完美 |
| 小米自带浏览器 | ✅ 完美 |
| 手机 Edge | ✅ 大部分正常 |
| 手机 Chrome | ⚠️ 需装 HttpServer 绕过 file:// 限制 |
| 桌面 Chrome/Edge | ✅ 完美 |

## 💡 为什么对话不是生硬的模板？

这是 v2 最大的升级。AI 会先阅读你的输入文件，理解文档主题（供应链？医学？法律？），然后**自动创建贴合主题的对话场景模板**。

比如输入是供应链文件 → 对话会讲供应商管理、交货周期、海关清关等，而不是「What does X mean?」那种教科书问法。

## 🏷️ 标签

`英语学习` `词汇` `HTML` `TTS` `神经网络音频` `edge-tts` `离线` `移动端` `生词提取`
