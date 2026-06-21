# 万能全平台自动答题脚本 - OpenAI 兼容接口版

基于 [【万能】全平台自动答题脚本](https://scriptcat.org/zh-CN/script-show-page/616) v5.3.0.2 修改，新增 **OpenAI 兼容接口答题**功能。

## ✨ 新增功能

在原有题库基础上，支持使用任意 OpenAI 兼容接口作为 AI 题库：

- **OpenAI**（gpt-4o-mini 等）
- **DeepSeek**（deepseek-chat）
- **通义千问**（qwen-plus）
- **Ollama**（本地部署，无需 API Key）
- 任何兼容 `/v1/chat/completions` 的接口

## 🔧 使用方式

1. 安装脚本（Tampermonkey / ScriptCat）
2. 点击答题面板的「更多设置」
3. 填写 OpenAI 配置：
   - **API 地址**：如 `https://api.openai.com/v1`
   - **API Key**：你的 key（本地 Ollama 可留空）
   - **模型名**：如 `gpt-4o-mini`、`deepseek-chat`
4. 保存即可生效

## 📋 工作逻辑

```
搜题 → 有 OpenAI 配置？ → 是 → 调 AI → 有结果？ → 返回
                    ↓ 否              ↓ 否
              走原有付费/免费题库 ←←←←←┘
```

优先使用 AI 答题，未配置或调用失败时自动回退到原有题库。

## 📖 支持平台

超星学习通、智慧树、职教云、雨课堂、考试星、优学院、青书学堂、学堂在线、英华学堂等数十个平台。

## ⚠️ 免责声明

本项目仅供学习交流使用。原脚本版权归原作者所有。

## 📄 License

MIT
