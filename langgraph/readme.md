# LangGraph学习剧本
*基于Google Gemini全栈LangGraph快速入门的分步学习计划*

## 🎯 项目概述

本项目是基于[Google Gemini全栈LangGraph快速入门](https://github.com/google-gemini/gemini-fullstack-langgraph-quickstart)的学习实践，旨在深度理解和掌握使用LangGraph构建研究增强型对话AI系统。

### 核心技术栈
- **前端**: React + Vite + TypeScript + Tailwind CSS + Shadcn UI
- **后端**: LangGraph + FastAPI + Google Gemini模型
- **工具**: Google Search API、Redis、PostgreSQL
- **部署**: Docker + Docker Compose

### 系统架构
本项目实现一个智能研究助手，能够：
1. 接收用户查询
2. 动态生成搜索词条
3. 通过Google Search API执行网络搜索
4. 分析搜索结果以识别知识缺口
5. 迭代优化搜索直到获得充分信息
6. 综合生成带引用的最终答案

## 📚 学习阶段规划

### 阶段1：环境搭建与基础理解（第1-2天）

#### 1.1 本地环境搭建
- [ ] 安装Node.js（推荐v18+）和npm/yarn
- [ ] 安装Python 3.8+
- [ ] 安装Docker和Docker Compose
- [ ] 配置Git环境

#### 1.2 API密钥准备
- [ ] 获取Google Gemini API密钥
  - 访问[Google AI Studio](https://makersuite.google.com/)
  - 创建新的API密钥
  - 记录密钥以便后续配置
- [ ] 获取LangSmith API密钥（可选，用于调试和监控）
  - 访问[LangSmith](https://smith.langchain.com/settings)
  - 创建账户并获取API密钥

#### 1.3 理论学习
- [ ] 阅读[LangGraph官方文档](https://langchain-ai.github.io/langgraph/)
- [ ] 理解Agent架构和状态图概念
- [ ] 学习RAG（检索增强生成）基础知识

### 阶段2：项目克隆与分析（第3天）

#### 2.1 获取源代码
```bash
# 克隆原始项目
git clone https://github.com/google-gemini/gemini-fullstack-langgraph-quickstart.git
cd gemini-fullstack-langgraph-quickstart

# 分析项目结构
tree -I 'node_modules|__pycache__|*.pyc'
```

#### 2.2 核心文件分析
- [ ] **`backend/src/agent/graph.py`** - 主要LangGraph逻辑
- [ ] **`backend/src/agent/state.py`** - 状态管理
- [ ] **`backend/src/agent/prompts.py`** - 提示词模板
- [ ] **`backend/src/agent/utils.py`** - 工具函数
- [ ] **`frontend/src/App.tsx`** - React主组件

#### 2.3 数据流理解
研究系统的数据流：
```
用户输入 → 初始查询生成 → 网络搜索 → 结果分析 → 知识缺口识别 → 迭代搜索 → 最终答案生成
```

### 阶段3：后端开发分步实践（第4-6天）

#### 3.1 第4天：基础Agent框架
- [ ] 创建基础LangGraph应用结构
- [ ] 实现状态定义（`state.py`）
- [ ] 创建配置管理（`configuration.py`）

**练习任务**：构建最简单的"Hello World" LangGraph Agent

#### 3.2 第5天：搜索与工具集成
- [ ] 集成Google Search API
- [ ] 实现搜索工具（`tools_and_schemas.py`）
- [ ] 创建查询生成节点

**练习任务**：实现能够接收用户输入并执行基础搜索的功能

#### 3.3 第6天：核心Agent逻辑
- [ ] 实现完整的图结构
- [ ] 添加反思和迭代逻辑
- [ ] 优化提示词设计

**练习任务**：完成核心Agent的搜索-分析-迭代循环

### 阶段4：前端开发（第7-8天）

#### 4.1 第7天：React应用基础
- [ ] 搭建Vite + React + TypeScript环境
- [ ] 配置Tailwind CSS和Shadcn UI
- [ ] 创建基础聊天界面

#### 4.2 第8天：前后端集成
- [ ] 实现与LangGraph API的通信
- [ ] 添加实时流式响应
- [ ] 优化用户界面和体验

### 阶段5：高级功能与优化（第9-10天）

#### 5.1 第9天：功能增强
- [ ] 添加对话历史管理
- [ ] 实现引用和来源显示
- [ ] 添加错误处理和重试机制

#### 5.2 第10天：部署与测试
- [ ] 配置Docker容器化
- [ ] 设置docker-compose部署
- [ ] 进行端到端测试

## 🛠 实践检查点

### 检查点1：基础环境（第2天结束）
- [ ] 成功运行原始项目
- [ ] 理解基础LangGraph概念
- [ ] API密钥配置完成

### 检查点2：后端理解（第6天结束）
- [ ] 独立构建基础Agent
- [ ] 实现搜索功能集成
- [ ] 理解状态图工作流

### 检查点3：全栈应用（第8天结束）
- [ ] 前后端通信成功
- [ ] 基础聊天功能可用
- [ ] 界面响应正常

### 检查点4：项目完成（第10天结束）
- [ ] 完整功能实现
- [ ] Docker部署成功
- [ ] 文档和代码注释完整

## 🔧 开发工具和资源

### 必备工具
- **IDE**: VS Code（推荐插件：Python、TypeScript、Tailwind CSS）
- **API测试**: Postman或Insomnia
- **数据库管理**: pgAdmin（PostgreSQL）或Redis Insight
- **版本控制**: Git + GitHub

### 学习资源
- [LangGraph文档](https://langchain-ai.github.io/langgraph/)
- [Google Gemini API文档](https://ai.google.dev/docs)
- [React + TypeScript指南](https://react-typescript-cheatsheet.netlify.app/)
- [FastAPI文档](https://fastapi.tiangolo.com/)

## 📝 每日学习日志模板

请在每天结束后在此记录学习进度：

### 第X天学习日志
- **学习内容**： 
- **完成任务**： 
- **遇到问题**： 
- **解决方案**： 
- **明日计划**： 

## 🚀 进阶挑战

完成基础学习后的扩展挑战：

1. **多模态集成**：添加图像搜索和分析功能
2. **知识图谱**：集成结构化知识存储
3. **个性化**：实现用户偏好学习
4. **性能优化**：实现搜索缓存和并行处理
5. **部署扩展**：添加Kubernetes部署配置

## 📞 获取帮助

遇到问题时，可通过以下方式寻求帮助：
- GitHub Issues（本项目）
- LangGraph Discord社区
- Stack Overflow（标签：langgraph、langchain）
- Google Gemini开发者论坛

---

**学习愉快！记住：熟能生巧，动手实践，多思考！** 🎉
