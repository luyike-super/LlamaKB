# LlamaKB

基于LlamaIndex和FastAPI构建的RAG（检索增强生成）知识库系统。

## 功能特点

- 基于LlamaIndex提供高效的文档检索
- 使用OpenAI API生成高质量回答
- RESTful API接口，易于集成
- 支持多种文档格式
- 简单易用的配置系统
- 可配置的CORS跨域资源共享

## 快速开始

### 安装依赖

```bash
pip install -r requirements.txt
```

### 配置环境变量

```bash
# 复制环境变量示例文件
cp .env.example .env
```

编辑`.env`文件，填入您的OpenAI API密钥和其他配置。

### 启动服务

使用启动脚本启动应用：

```bash
# 默认配置启动
python run.py

# 自定义主机和端口
python run.py --host 0.0.0.0 --port 8000
```

或直接使用uvicorn:

```bash
# 开发模式（自动重载）
uvicorn app.main:app --reload

# 生产模式
uvicorn app.main:app
```

服务将在 http://localhost:8000 上启动，您可以访问 http://localhost:8000/api/v1/docs 查看API文档。

## 项目结构

```
app/
├── api/                # API定义
│   └── v1/             # API版本1
│       └── endpoints/  # API端点
├── core/               # 核心配置
├── models/             # 数据模型
├── services/           # 业务逻辑
└── utils/              # 工具函数
```

## API文档

启动服务后，访问 http://localhost:8000/api/v1/docs 查看Swagger文档。
