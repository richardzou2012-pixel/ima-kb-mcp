# ima-kb-mcp（托管配置）

腾讯 ima 知识库的 MCP 服务，用于在魔搭 MCP 广场托管部署。

服务本体来自 PyPI 包 [ima-kb-mcp](https://pypi.org/project/ima-kb-mcp/)，通过 `uvx` 直接运行，本仓库只存放部署配置。

## 功能

- 搜索 / 列出知识库
- 浏览知识库内容（含文件夹）
- 在知识库内全文搜索
- 获取文件原文地址
- 搜索笔记、读取笔记正文

## 服务配置

```json
{
  "mcpServers": {
    "ima-kb": {
      "command": "uvx",
      "args": ["ima-kb-mcp"],
      "env": {
        "IMA_OPENAPI_CLIENTID": "",
        "IMA_OPENAPI_APIKEY": ""
      }
    }
  }
}
```

## 环境变量

| 变量 | 说明 |
| --- | --- |
| `IMA_OPENAPI_CLIENTID` | IMA OpenAPI 的 Client ID |
| `IMA_OPENAPI_APIKEY` | IMA OpenAPI 的 API Key |

凭证获取：https://ima.qq.com/agent-interface
