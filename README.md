# GLM-5.3 Flash API (glm-5.3-flash / glm5.3flash) — llm guide with published pricing

> **input $0.06; cached_input $0.012; output $0.2** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://go.apimart.ai/k-0b77e6)** · **[Get an API key](https://go.apimart.ai/k-9554ca)**

Everything here refers to **glm-5.3-flash** — also written **glm5.3flash** or **glm 5.3 flash**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `input` | $0.06 |
| `cached_input` | $0.012 |
| `output` | $0.2 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $6 |
| 1,000 | $60 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"glm-5.3-flash","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
