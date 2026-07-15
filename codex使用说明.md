## 配置模型--打开vscode

#### 1.手动配置
#### **配置神马中转API作为第三方API**

Codex CLI 会读取你的配置文件：一般在 ~/.codex/（Windows 也是用户目录下的 .codex）。创建两份文件：

- auth.json：放密钥
    
- config.toml：放模型与网关配置


**auth.json（把 sk-xxx 换成你的神马中转API Key）**


```plaintext
{"OPENAI_API_KEY": "sk-xxx"}
```


**config.toml**


```plaintext

model_provider = "whatai"
model = "gpt-5-codex"
model_reasoning_effort = "high"
disable_response_storage = true
preferred_auth_method = "apikey"

[model_providers.whatai]
name = "whatai"
base_url = "https://api.whatai.cc/v1"
wire_api = "responses"
```


![](assets/codex使用说明/file-20260715114822473.mp4)


#### 2.直接让codex配置
