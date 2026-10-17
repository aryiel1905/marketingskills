# Multi-project marketing context

Use this routing when a user works on more than one brand, client, or product. Resolve one context before drafting; never combine facts, voice, proof, or approvals from different projects.

1. If the request names a project, select its context under `.agents/marketing-contexts/<project-slug>.md` in the user's project workspace. Confirm the file's `Project` field matches the request. A named project overrides any active pointer.
2. Otherwise, if `.agents/active-marketing-context.md` exists, read its `Context file` path, resolve it relative to the workspace, and confirm that file's `Project` field fits the request. Do not follow a stale or conflicting pointer.
3. Otherwise, use the project's `.agents/product-marketing.md`. Older `.claude/product-marketing.md` and `product-marketing-context.md` remain fallbacks.
4. If multiple contexts plausibly match, ask which project applies. If the selected file is missing, continue with facts supplied in the current request, label gaps, and offer to draft a context file. Never silently borrow another project's context.

An optional pointer contains only:

```markdown
# Active marketing context
Context file: .agents/marketing-contexts/<project-slug>.md
```

Each context uses the product-marketing structure and begins with `Project: <name>` and `Context scope: <client, independent product, or academic project>`. Keep actual client data, contact lists, private campaign results, and unpublished claims in that project's workspace, not in a public skills fork. Example starter files are in `../assets/property-development.example.md` and `../assets/indie-product.example.md`; copy one into the selected project workspace and replace placeholders. An example is never evidence for a live claim.

For any claim, record its source, as-of date, approval status, and scope in the context's Proof Points or Learnings section. Treat a target return as a target, not a realized outcome. Use a project's voice and language preferences only for that project.
