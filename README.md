# 401/403 Bypass Techniques — Expert Attack Playbook

A comprehensive playbook for testing what happens when the server says "access denied" — and whether that denial actually holds.

## What it is

A skill covering the full matrix of 401/403 forbidden bypass techniques: path manipulation, HTTP method tampering, header injection, protocol downgrade, and automated bypass tools. Base models typically know 2–3 header bypasses but miss the path-manipulation variants and verb+path combinations.

**Technique families:**

- **Path manipulation** — trailing slash/dot, case sensitivity, URL encoding, double encoding, semicolon and null-byte tricks
- **Method tampering** — verb override (`X-HTTP-Method-Override`), HEAD/OPTIONS probing
- **Header injection** — `X-Original-URL`, `X-Forwarded-For`, `X-Rewrite-URL`
- **Protocol tricks** — HTTP version downgrade, HTTP/2 smuggling past proxy ACLs
- **Combination attacks** — verb + path + header combos

## What's inside

- `SKILL.md` — the full playbook with payloads, examples, and when each technique works

## Related skills

- `authbypass-authentication-flaws` — broader auth bypass (login flaws, session handling)
- `waf-bypass-techniques` — when the bypass is WAF-specific rather than access control
- `http-host-header-attacks` — Host header manipulation for routing bypass
- `request-smuggling` — smuggle past access controls entirely

## Scope & Authorization

Authorized testing only — bug bounty programs (in-scope targets only), pentest engagements, or CTFs. Only test targets you own or have explicit written authorization for. A bypass that works is a finding to report, not an invitation to access data you are not authorized to see.

## License

MIT — see [LICENSE](LICENSE).
