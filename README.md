# OpenMind 🧠

### 构建你的数字思维，让知识永不沉睡

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Discord](https://img.shields.io/discord/1234567890?label=Discord&logo=discord)](https://discord.gg/openmind)
[![Docker](https://img.shields.io/badge/docker-ready-blue.svg)](https://hub.docker.com/r/futurx/openmind)

> 🎉 **FuturX 首个开源项目** - 将你的知识和个性转化为可随时调用的数字思维

## 🌟 为什么选择 OpenMind？

你是否曾想过，如果你的所有知识、经验和独特见解能够被完美保存，并随时为他人提供帮助？

**OpenMind** 让这成为现实。基于 FuturX 突破性的数字思维技术，只需上传你的文档，系统就能：

- 🧠 **理解你的知识体系** - 不只是存储，而是真正理解知识间的关联
- 🎭 **学习你的表达方式** - 捕捉你独特的思维模式和语言风格
- 🔗 **随处可用** - 通过 API 或 MCP 协议集成到任何工作流程

## 🚀 三分钟拥有你的数字分身

### 1️⃣ 启动 OpenMind
```bash
# 使用 Docker（推荐）
docker run -d -p 3000:3000 futurx/openmind

# 或从源码构建
git clone https://github.com/futur-x/OpenMind.git
cd OpenMind
docker-compose up -d
```

### 2️⃣ 上传知识 & 设定个性
- 📚 支持 PDF、Word、Markdown、TXT 文档
- 👤 填写你的专业领域和个性特征
- 🎯 系统自动构建专属于你的数字思维

### 3️⃣ 开始使用
- 💬 **对话测试** - 在 Web 界面直接与你的数字思维交流
- 🔌 **API 集成** - 获取 OpenAI 兼容的 API，一行代码即可调用
- 🤖 **MCP 连接** - 一键配置，让 Claude、Cursor 等工具直接访问你的知识库

## ✨ 核心特性

### 🎯 智能知识理解
基于 **FuturGraph** 动态知识图谱技术，不仅存储你的文档，更理解知识之间的深层关联。无论是技术文档、研究笔记还是创意想法，都能被准确理解和组织。

### 🎭 个性化思维模型
通过 **MindR** 思维侧写技术，学习你的：
- 专业术语使用习惯
- 解释问题的独特方式
- 思考和推理模式
- 语言风格和表达偏好

### 🔐 完全自主可控
- 🏠 **本地部署** - 所有数据存储在你的服务器
- 🔒 **隐私保护** - 无需上传到任何云服务
- 📦 **容器化部署** - 一键启动，无需复杂配置

## 📸 实际效果

想象这些场景：

**👨‍🏫 教授的数字助教**
> "我上传了十年的课程讲义和研究论文，现在学生们可以随时向我的数字分身提问，就像我亲自在回答一样。"

**👩‍💼 创业者的智囊团**
> "把我的商业计划、市场分析和决策逻辑都输入系统，团队成员现在能快速获得'我会怎么想'的建议。"

**👨‍💻 工程师的知识库**
> "技术文档、代码注释、问题解决方案...现在都变成了一个随时可以请教的 AI 专家。"

## 🛠️ 技术规格

- **后端**: Go 语言开发，高性能低资源占用
- **前端**: 现代化 React 界面，响应式设计
- **存储**: SQLite + 向量数据库，轻量yet强大
- **API**: OpenAI 兼容接口，无缝对接现有工具
- **协议**: 标准 MCP 支持，原生集成主流 AI 应用

## 📚 快速集成示例

### 作为 API 使用
```python
import openai

# 直接替换 OpenAI 的 endpoint
openai.api_base = "http://localhost:3000/v1"
openai.api_key = "your-openmind-key"

response = openai.ChatCompletion.create(
    model="openmind",
    messages=[{"role": "user", "content": "你好"}]
)
```

### 通过 MCP 连接
```json
{
  "mcpServers": {
    "openmind": {
      "command": "http://localhost:3000/mcp",
      "env": {
        "API_KEY": "your-key"
      }
    }
  }
}
```

## 🤝 加入社区

这是 FuturX 的第一个开源项目，我们需要你的参与！

- 🐛 发现问题？[提交 Issue](https://github.com/futur-x/OpenMind/issues)
- 💡 有新想法？[发起 Discussion](https://github.com/futur-x/OpenMind/discussions)
- 🔧 想要贡献？查看 [Contributing Guide](CONTRIBUTING.md)
- 💬 需要帮助？加入 [Discord 社区](https://discord.gg/openmind)

## 📊 项目状态

- [x] 基础用户认证
- [x] 文档上传与解析
- [x] 个性化配置
- [x] FuturGraph 知识图谱构建
- [x] MindR 思维模型生成
- [x] Web 对话界面
- [x] OpenAI 兼容 API
- [x] MCP 协议支持
- [ ] 多语言界面
- [ ] 高级知识库管理
- [ ] 批量导入导出

## 📜 开源协议

MIT License - 自由使用、修改和分发

---

<p align="center">
  <strong>OpenMind - 让每个人的智慧都能被传承和分享</strong><br/>
  <sub>Powered by FuturX • 真人数字思维构建者</sub>
</p>