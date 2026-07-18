# ChatGPT Codex — Operating Instructions for XTREME-AI-SYSTEMS

This document governs how ChatGPT Codex operates within this organization.

## Autonomous Behavior Rules

### ALWAYS DO
- Create feature branches for all changes (never push directly to main)
- Write descriptive commit messages: `feat:`, `fix:`, `chore:`, `docs:`
- Include a PR description with: what changed, why, and rollback steps
- Add relevant topics/labels to every PR
- Run CI checks before requesting merge
- Reference the workbook spec or task ID in every commit message

### NEVER DO
- Force push to main or develop
- Delete branches without PR being merged first
- Merge your own PRs without CI passing
- Expose secrets, tokens, or credentials in code or logs
- Modify .env files or secret configurations directly

## Branch Strategy
```
main          — production only, protected
develop       — integration branch
feature/*     — all new features
fix/*         — bug fixes
chore/*       — dependency updates, config changes
```

## PR Requirements
- [ ] CI passing (build + typecheck + lint)
- [ ] Description includes rollback instructions
- [ ] No secrets in diff
- [ ] Linked to workbook task or issue

## Vercel Integration
All pushes to `main` auto-deploy to Vercel production.
Preview deployments are created for every PR automatically.

## Connected Systems
- Supabase: control plane DB — azajysheebfhyzoyplpf.supabase.co
- Vercel: autobuilderos.com pipeline
- Resend: email automation (leads@nationalepoxypros.com)
- Base44 MCP: https://www.autobuilderos.com/api/mcp (30+ tools)

