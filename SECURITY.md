# Security Policy

## Supported versions

| Version | Supported |
| ------- | --------- |
| `main`  | ✅ Yes    |
| Older   | ❌ No     |

## Reporting a vulnerability

**Please do not open a public issue for security problems.**

1. Go to the repository's **Security** tab and choose **Report a vulnerability** (private advisory), or
2. Contact the maintainer, [@swapnilchaudhari007](https://github.com/swapnilchaudhari007), directly.

Please include:

- A description of the issue and its impact
- Steps to reproduce, or a proof of concept
- Affected files, endpoints or features
- Any suggested fix

### What to expect

| Step | Target time |
| ---- | ----------- |
| Acknowledgement | within 72 hours |
| Initial assessment | within 7 days |
| Fix or mitigation | depends on severity |

Reporters are credited in the release notes unless they'd rather stay anonymous.

## Areas of special concern

Because this project covers **AI-powered GitHub app features**, we especially want reports about:

- **Prompt injection:** issue text, PR descriptions, commit messages or file contents that can steer an AI feature into unintended actions
- **Token and secret exposure:** GitHub App private keys, installation tokens, webhook secrets or AI provider API keys leaking into logs, responses or model context
- **Over-scoped permissions:** features that request more GitHub App permissions than they need
- **Webhook verification:** missing or weak `X-Hub-Signature-256` validation
- **Data leakage:** private repository content sent to third-party AI services without disclosure

## Best practices for contributors

- Never commit secrets; use environment variables or GitHub Actions secrets
- Treat all repository content as untrusted input to any AI model
- Request the minimum GitHub App permissions needed
- Verify every incoming webhook signature
- Redact tokens and personal data from logs
