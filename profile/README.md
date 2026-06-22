# Hi there 👋

**upcloud-tools** is a third-party collection of tools, drivers, and utilities for the [UpCloud](https://upcloud.com) cloud platform.

> ⚠️ This organization is **not affiliated with, endorsed by, or connected to UpCloud Ltd.** These are community-maintained projects.

## What's here

- **upcloud-csi** [link](https://github.com/upcloud-tools/upcloud-csi) — A Container Storage Interface (CSI) driver for Kubernetes, forked from the official UpCloud driver with additional features like online volume resizing.

## Repository Security

This repository uses the following security and supply-chain measures:

- **Security policy** — `SECURITY.md` directs reporters to GitHub's Private vulnerability reporting tool.
- **Vulnerability reporting** — Private vulnerability reporting enabled; reporters get an acknowledgment within 72 hours.
- **Code scanning (CodeQL)** — `github/codeql-action` analyzes Go code on every push/PR to `main` and weekly. Maintainability and Reliability scores are **Excellent** (0 findings).
- **Dependabot alerts** — Monitors Go modules, GitHub Actions, and Docker dependencies daily with alerts for vulnerable dependencies.
- **Secret scanning** — GitHub's built-in secret scanning alerts enabled at the repository level.
- **Branch protection** — `main` requires passing status checks (`golangci-lint`, `helm-lint`, `test`, CodeQL) and pull request review before merge.
- **Action pinning** — All GitHub Actions pinned by commit SHA with a human-readable version comment; enforced globally.
- **Static analysis** — `golangci-lint` with 50+ linters (`gosec`, `staticcheck`, `errcheck`, etc.) runs on every PR.
- **Container scanning (Trivy)** — `aquasecurity/trivy-action` scans the built image for OS and application CVEs before push to GHCR; scheduled weekly rescan catches newly discovered vulnerabilities. Go module dependencies also scanned on every push/PR.
- **Container signing (Cosign)** — Release images are signed via keyless `cosign sign` using GitHub OIDC.
- **Release integrity** — Helm chart validates that `appVersion` matches the git tag and that the container image exists before publishing.
- **Artifact Hub** — Helm chart metadata published to Artifact Hub for discoverability.

## Contributing

PRs and issues welcome. See individual project repos for contribution guidelines.

## Resources

- [UpCloud API docs](https://www.upcloud.com/docs/api/)
- [Kubernetes CSI docs](https://kubernetes-csi.github.io/docs/)
