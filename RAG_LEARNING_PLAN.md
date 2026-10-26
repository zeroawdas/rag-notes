# RAG 学习路线与面试作品集计划

> **目标**：零基础 → 完成 3 个 RAG 项目 → 拿到面试机会  
> **总周期**：约 4 周  
> **GitHub 用户名**：zeroawdas  
> **开始日期**：2026/05/31

---

## 项目总览

| 序号 | 项目名称 | 难度 | 时间 | 产出 | 面试价值 |
|------|----------|------|------|------|----------|
| ~~1~~ | ~~MaxKB 部署体验~~ | ⭐ | 跳过 | - | Docker 未安装，跳过 |
| **2** | **rag-from-scratch 跟练** | ⭐⭐ | 1-2 周 | GitHub 仓库 | **进行中** |
| 3 | 自建文档问答系统 | ⭐⭐⭐ | 2-3 周 | GitHub 仓库 + README | **作品集核心** |
| 加分 | RAG_Techniques 进阶 | ⭐⭐⭐⭐ | 按需 | 学习笔记 | 面试加分项 |

---

## 项目一：MaxKB 部署体验

**仓库**：[1Panel-dev/MaxKB](https://github.com/1Panel-dev/MaxKB) ⭐ 11.3k  
**目标**：不写代码，先看 RAG 能做什么  
**任务清单**：

- [ ] 安装 Docker Desktop
- [ ] 运行 `docker run -d --name=maxkb -p 8080:8080 1panel/maxkb`
- [ ] 上传一份 PDF 文档
- [ ] 基于文档内容提问，观察回答效果
- [ ] 截图记录整个流程

**产出**：一篇体验笔记（可作为博客/面试谈资）

---

## 项目二：rag-from-scratch 跟练

**仓库**：[Lanqingsong/rag-from-scratch](https://github.com/Lanqingsong/rag-from-scratch)  
**目标**：跟着 19 篇中文教程，理解 RAG 每一步原理  
**技术栈**：LangChain + DeepSeek + FAISS + BM25

**核心知识点**：

| 模块 | 内容 | 状态 |
|------|------|------|
| 文档加载 | PDF/TXT/DOCX 读取解析 | ⬜ |
| 文本分块 | Chunking 策略、重叠窗口 | ⬜ |
| 向量嵌入 | Embedding 原理、模型选择 | ⬜ |
| 向量存储 | FAISS 索引与检索 | ⬜ |
| 混合检索 | BM25 关键词 + 向量语义 | ⬜ |
| 重排序 | Reranker 优化检索结果 | ⬜ |
| Prompt 构建 | 检索结果拼接 + 提示词设计 | ⬜ |
| LLM 生成 | DeepSeek API 调用 | ⬜ |

**产出**：自己的 GitHub 仓库，包含跑通的代码和注释

---

## 项目三：自建文档问答系统（核心作品）

**目标**：从零搭建一个完整的 RAG 应用  
**功能**：
- 支持上传 PDF / DOCX / TXT 多种格式
- 文档内容自动分块、向量化存储
- 用户提问 → 检索相关段落 → LLM 生成答案
- Streamlit / Gradio Web 界面
- 显示引用来源（哪份文档的哪一段）

**技术选型（参考）**：
- Python 3.10+
- LangChain
- FAISS（本地向量库）
- DeepSeek API（国内可用）
- Streamlit（前端 UI）

**产出**：一个完整的 GitHub 仓库，包含：
- `app.py` 主程序
- `requirements.txt` 依赖
- `README.md` 项目说明（使用模板）

---

## 面试准备清单

### 必须能讲清楚的概念

- [ ] **RAG 是什么**：检索增强生成，解决 LLM 幻觉和知识时效性问题
- [ ] **Embedding 原理**：文本 → 高维向量 → 语义相近的文本向量距离近
- [ ] **分块策略**：为什么分块？块大小怎么选？重叠窗口的作用？
- [ ] **向量检索流程**：查询向量化 → 相似度计算（余弦相似度）→ Top-K 召回
- [ ] **混合检索**：BM25 关键词匹配 + 向量语义匹配，互补优势
- [ ] **Rerank 的作用**：初筛 → 精排，提升最终结果相关性
- [ ] **RAG 的典型问题**：检索不准、上下文过长、多跳推理失败

### 面试常见问题

| 问题 | 准备方向 |
|------|----------|
| 你做的 RAG 项目解决了什么问题？ | 准备 1 分钟电梯演讲 |
| 为什么用 FAISS 而不是其他向量库？ | 了解 FAISS vs Chroma vs Milvus |
| 分块大小怎么选的？ | 准备实际数据对比 |
| 如果你做的系统准确率只有 60%，怎么优化？ | 检索优化、Rerank、Prompt 调优 |
| RAG 和微调的区别？什么时候用哪个？ | 成本、时效性、数据量对比 |

---

## 学习资源

### GitHub 参考仓库

| 仓库 | 星标 | 用途 |
|------|------|------|
| [1Panel-dev/MaxKB](https://github.com/1Panel-dev/MaxKB) | 11.3k | 快速体验 |
| [Lanqingsong/rag-from-scratch](https://github.com/Lanqingsong/rag-from-scratch) | - | 跟练学习 |
| [NirDiamant/RAG_Techniques](https://github.com/NirDiamant/RAG_Techniques) | 26.9k | 进阶参考 |
| [jamwithai/production-agentic-rag](https://github.com/jamwithai/production-agentic-rag-course) | 4.8k | 工程化 |
| [HKUDS/LightRAG](https://github.com/HKUDS/LightRAG) | 34k | 知识图谱 RAG |

### 必备账号

- [x] GitHub 账号
- [x] DeepSeek API Key（[platform.deepseek.com](https://platform.deepseek.com)）
- [x] 阿里云 DashScope API Key

---

## 进度记录

| 日期 | 完成事项 | 备注 |
|------|----------|------|
| 2026/05/31 | 克隆 rag-from-scratch，安装依赖 | Python 3.14.4，使用清华镜像 |
| 2026/05/31 | 配置 DeepSeek + DashScope API Key | 两个 Key 均已配置 |
| 2026/05/31 | 解决 FAISS 中文路径问题 | 项目移至非中文路径目录 |
| 2026/05/31 | 系统成功启动，创建测试文档 | http://127.0.0.1:5000 可访问 |
| 2026/05/31 | 首次 RAG 问答测试通过 | 基于 Python 知识文档问答成功 |
