# CodeCargo

**The Control Plane for GitHub.**

CodeCargo is the AI-powered Internal Developer Portal for GitHub, purpose-built
to orchestrate agentic workflows across the entire software lifecycle. We help
enterprises tame GitHub at scale — consolidating DevOps tooling, automating
compliance, securing CI/CD, and giving developers self-service superpowers.

[codecargo.com](https://codecargo.com) · [Documentation](https://docs.codecargo.com)

---

## What we build

- **GitHub Migration** — Translate legacy pipelines from Jenkins, GitLab CI,
  CircleCI, and others into modern GitHub Actions with AI-assisted authoring.
- **Workflow Guardrails** — Enforce security policies, compliance checks, and
  org standards across every workflow, with drift detection and audit evidence.
- **CargoWall** — Kernel-level eBPF firewall for GitHub Actions runners.
- **Developer Self-Service** — Multi-repo edits with GenAI, a private Actions
  marketplace, an agentic service catalog, and UI-callable automations.

Built for enterprise scale. GitHub native. SOC 2 Type II.

## Open source

We ship the security primitives we rely on in the open.

- **[cargowall](https://github.com/code-cargo/cargowall)** — eBPF-based network
  firewall for GitHub Actions runners. Kernel-level egress filtering, dynamic
  DNS resolution, full process attribution, NDJSON audit logs. Audit and
  enforce modes.
- **[cargowall-action](https://github.com/code-cargo/cargowall-action)** — The
  official GitHub Action. Drop one step into your workflow to lock down egress
  with hostname globs and CIDR rules:

  ```yaml
  jobs:
    cargowall-example:
      permissions:
        id-token: write
        actions: read
        contents: read
      steps:
      - uses: code-cargo/cargowall-action@v1
        with:
          # run in audit to learn what your job egress needs
          mode: audit
  ```

## Get in touch

- Website: [codecargo.com](https://codecargo.com)
- Docs: [docs.codecargo.com](https://docs.codecargo.com)
- Email: [info@codecargo.com](mailto:info@codecargo.com)
