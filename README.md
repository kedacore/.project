# KEDA `.project`

`.project` (dot-project) is a CNCF initiative to centralize and automate metadata management for all CNCF projects.
This repository holds the canonical metadata for [KEDA](https://keda.sh/) and is maintained by the CNCF automation tooling.

## What's in this repo

| File | Purpose |
|------|---------|
| `project.yaml` | Canonical project metadata (name, maturity, repositories, governance links, …) |
| `maintainers.yaml` | Maintainer and reviewer roster used for drift detection and mailing-list sync |
| `ADOPTERS.md` | Reference to KEDA's public adopters list and instructions for joining it |
| `CODEOWNERS` | Ensures PRs to this repo require maintainer approval |
| `.github/workflows/validate.yaml` | CI — validates `project.yaml` and `maintainers.yaml` on every PR |
| `.github/workflows/update-landscape.yml` | Automatically proposes landscape updates when `project.yaml` changes |

## Keeping metadata up to date

Open a pull request against this repository to update any metadata field.
The validate workflow will check schema correctness and block merge if validation fails.

> **Note:** This repository was bootstrapped automatically from public sources (CNCF landscape, CLOMonitor, GitHub governance files).
> Project maintainers should verify metadata against the project's current sources when updating it.

## Maintainer LFID setup

Every member of a managed team in `maintainers.yaml` must:

- Have a Linux Foundation ID (LFID) at [openprofile.dev](https://openprofile.dev/).
- Link the GitHub account listed in `maintainers.yaml` to that LFID.
- Verify the primary email address and company affiliation on the profile.

LFID setup is confirmed manually. Automated LFX account verification remains
disabled pending the [upstream long-lived token issue](https://github.com/cncf/automation/issues/293).
Project and maintainer schema validation remains enabled.

## Resources

- [`.project` documentation](https://github.com/cncf/automation/tree/main/utilities/dot-project)
- [Schema reference](https://github.com/cncf/automation/blob/main/utilities/dot-project/SCHEMA.md)
- [CNCF Automation repository](https://github.com/cncf/automation)
