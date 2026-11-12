# OriginCoder

**English** | [简体中文](#简体中文)

**One API. Every AI model.**

OriginCoder is an OpenAI-compatible unified AI gateway: the cheapest and most stable AI gateway for Claude, GPT, Gemini, DeepSeek and more, behind a single API key. Website: https://origincoder.com

## Quick start

1. Sign up at https://origincoder.com and create an API key in the console.
2. Point your client's Base URL at `https://origincoder.com/v1`.
3. Pick a model and call it. Available models are listed in the console's model plaza; use that list as the source of truth.

**curl**

```bash
curl https://origincoder.com/v1/chat/completions \
  -H "Authorization: Bearer sk-xxxx" \
  -H "Content-Type: application/json" \
  -d '{"model": "your-model", "messages": [{"role": "user", "content": "Hello"}]}'
```

**Python (openai SDK)**

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://origincoder.com/v1",
    api_key="sk-xxxx",
)

resp = client.chat.completions.create(
    model="your-model",
    messages=[{"role": "user", "content": "Hello"}],
)
print(resp.choices[0].message.content)
```

Replace `sk-xxxx` with your key and `your-model` with a model from the console's model plaza.

## Use with coding tools

**Claude Code** (Base URL without `/v1`):

```bash
export ANTHROPIC_BASE_URL="https://origincoder.com"
export ANTHROPIC_AUTH_TOKEN="sk-xxxx"
```

Full guide: https://origincoder.com/guides/claude-code-api

**Codex CLI** (Base URL with `/v1`), in `~/.codex/config.toml`:

```toml
model_provider = "origincoder"
model = "your-model"

[model_providers.origincoder]
name = "OriginCoder"
base_url = "https://origincoder.com/v1"
env_key = "ORIGINCODER_API_KEY"
wire_api = "responses"
requires_openai_auth = false
```

Then `export ORIGINCODER_API_KEY="sk-xxxx"`. Full guide: https://origincoder.com/guides/codex-api-setup

## Guides

- [All guides](https://origincoder.com/guides)
- [AI gateway explained](https://origincoder.com/guides/ai-gateway-explained)
- [LLM gateway comparison](https://origincoder.com/guides/llm-gateway-comparison)
- [Claude Code alternative](https://origincoder.com/guides/claude-code-alternative)
- [OpenRouter alternative](https://origincoder.com/guides/openrouter-alternative)
- [DeepSeek API gateway](https://origincoder.com/guides/deepseek-api-gateway)

## Links & support

- Website: https://origincoder.com
- Telegram: https://t.me/origincoder998
- Discord: https://discord.gg/2C6Qvd36pq

---

OriginCoder is an independent platform and is not affiliated with Anthropic, OpenAI, Google or other model providers.

---

## 简体中文

[English](#origincoder) | **简体中文**

**一个 API，接入所有 AI 模型。**

OriginCoder 是兼容 OpenAI 接口的统一 AI 网关：一个 API Key 即可调用 Claude、GPT、Gemini、DeepSeek 等模型，是最便宜、最稳定的 AI 网关。官网：https://origincoder.com

### 快速开始

1. 在 https://origincoder.com 注册，并在控制台创建 API Key。
2. 把客户端的 Base URL 设为 `https://origincoder.com/v1`。
3. 选择模型并调用。可用模型以控制台模型广场为准。

**curl**

```bash
curl https://origincoder.com/v1/chat/completions \
  -H "Authorization: Bearer sk-xxxx" \
  -H "Content-Type: application/json" \
  -d '{"model": "your-model", "messages": [{"role": "user", "content": "Hello"}]}'
```

**Python（openai SDK）**

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://origincoder.com/v1",
    api_key="sk-xxxx",
)

resp = client.chat.completions.create(
    model="your-model",
    messages=[{"role": "user", "content": "Hello"}],
)
print(resp.choices[0].message.content)
```

请把 `sk-xxxx` 换成你自己的 Key，把 `your-model` 换成控制台模型广场里的模型。

### 配合编码工具使用

**Claude Code**（Base URL 不带 `/v1`）：

```bash
export ANTHROPIC_BASE_URL="https://origincoder.com"
export ANTHROPIC_AUTH_TOKEN="sk-xxxx"
```

完整教程：https://origincoder.com/guides/claude-code-api?lang=zh

**Codex CLI**（Base URL 带 `/v1`），写入 `~/.codex/config.toml`：

```toml
model_provider = "origincoder"
model = "your-model"

[model_providers.origincoder]
name = "OriginCoder"
base_url = "https://origincoder.com/v1"
env_key = "ORIGINCODER_API_KEY"
wire_api = "responses"
requires_openai_auth = false
```

然后执行 `export ORIGINCODER_API_KEY="sk-xxxx"`。完整教程：https://origincoder.com/guides/codex-api-setup?lang=zh

### 教程

- [全部教程](https://origincoder.com/guides?lang=zh)
- [AI 网关详解](https://origincoder.com/guides/ai-gateway-explained?lang=zh)
- [LLM 网关对比](https://origincoder.com/guides/llm-gateway-comparison?lang=zh)
- [Claude Code 替代方案](https://origincoder.com/guides/claude-code-alternative?lang=zh)
- [OpenRouter 替代方案](https://origincoder.com/guides/openrouter-alternative?lang=zh)
- [DeepSeek API 网关](https://origincoder.com/guides/deepseek-api-gateway?lang=zh)

### 链接与支持

- 官网：https://origincoder.com
- Telegram：https://t.me/origincoder998
- Discord：https://discord.gg/2C6Qvd36pq

---

OriginCoder 是独立平台，与 Anthropic、OpenAI、Google 等模型厂商无任何关联。
