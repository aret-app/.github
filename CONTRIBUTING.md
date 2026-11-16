# Contributing to Aret

Thanks for helping build Aret! This guide applies to every repository in the organization unless a repository has its own `CONTRIBUTING.md`.

## Where things live
- **Work tracking:** all issues from all repos appear on the org project board **Aret Roadmap**.
- **Ideas and design discussions:** GitHub Discussions on `aret-docs`. Accepted ideas become issues.
- **Architecture decisions:** ADRs in `aret-docs/docs/adr/`. A significant technical choice gets an ADR pull request.

## Workflow
1. Pick an issue (or open one first for anything non-trivial) and assign yourself.
2. Create a branch from `main`: `feat/<short-name>`, `fix/<short-name>`, `chore/<short-name>`.
3. Commit using [Conventional Commits](https://www.conventionalcommits.org/): `feat(tracks): add GPX export`.
4. Sign off every commit (`git commit -s`), see *Developer Certificate of Origin* below.
5. Open a pull request, link the issue (`Closes #123`), fill in the template.
6. `main` is protected: changes only land through a PR, and required CI checks must pass. We squash-merge.
   **During the prototype phase the core team doesn't review each other's PRs** (0 approvals required), so run the
   checks locally before opening a PR and call out risky changes (migrations, auth, secrets) in its description.
   Outside contributions are still reviewed by a maintainer.

## Developer Certificate of Origin (DCO)
By signing off a commit you certify that you wrote the code or have the right to submit it under the repository's license ([developercertificate.org](https://developercertificate.org/)). Use `git commit -s` to add the `Signed-off-by:` line.

## Code style
- **Swift:** SwiftLint + swift-format; prefer small Swift packages per feature.
- **Rust:** `cargo fmt`, `cargo clippy -- -D warnings`, `cargo deny check`.
- Tests are required for new behavior.

## Map data problems
Most wrong trails, names or POIs come from OpenStreetMap. Please fix them at the source on [openstreetmap.org](https://www.openstreetmap.org/) — the fix will reach Aret on the next map rebuild.

## Security
Never open a public issue for a vulnerability. See [SECURITY.md](SECURITY.md).
