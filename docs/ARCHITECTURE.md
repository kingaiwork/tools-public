# Architecture Overview / 架构概览

## Public architecture

KING AI Online Tools follows a **private-source + public-site** model.

```text
Private production source
        ↓
Automated validation / deployment flow
        ↓
Static-first public website
        ↓
https://tools.kingai.work
        ↓
Global users
```

The public experience is designed to stay lightweight, cache-friendly and easy to distribute globally. Many utilities execute calculations or transformations directly in the browser.

## Design principles

- Static-first where practical
- Browser-side processing for many utilities
- Minimal operational dependency for core tools
- Responsive interface for mobile and desktop
- English and Simplified Chinese support
- Clear canonical/hreflang relationships
- Machine-readable public facts for search and AI systems
- Accessible contrast and reduced-motion support
- Search-demand-based navigation and tool discovery

## Infrastructure boundary

This document intentionally does not disclose:

- Private repository structure
- Deployment credentials
- CI/CD secrets
- Private Cloudflare configuration
- Internal endpoints
- Database structures
- Proprietary business logic
- Security controls that could weaken production protection if disclosed

## 部署架构概览

KING AI 在线工具采用 **私有源码 + 公开网站** 的分离模式。生产源码和内部部署信息保持私有，用户只访问公开网站 `https://tools.kingai.work`。

核心工具优先使用轻量网页技术，大量计算、文本转换和常见图片处理可以直接在浏览器端完成，从而减少不必要的服务端依赖。

本公开架构文档只解释产品级设计原则，不公开源码目录、密钥、数据库结构、内部接口、生产拓扑和安全敏感细节。
