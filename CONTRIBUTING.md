# Contributing to scoop-osf

This repository is a Scoop bucket for OSF CLI Go. Contributions should maintain correct Windows release metadata, architecture mappings, checksums and update behaviour.

## Before you start

Read [README.md](README.md) and the existing manifest under [bucket](bucket). Check current pull requests and the corresponding OSF CLI Go release before changing versions. Keep changes to the application itself in its source repository and explain any compatibility change for installed users.

For bugs, provide the affected version or commit, environment, minimal reproduction, expected result and observed result. For a substantial proposal, describe the use case and compatibility impact before expanding implementation scope. Use existing issue templates when offered.

## Development and validation

The documented installation smoke path is:

```powershell
scoop bucket add osf https://github.com/edithatogo/scoop-osf
scoop install osf-cli-go
osf --version
```

Use a suitable development machine and record Windows version, architecture and installed version. Report untested architectures explicitly. For manifest edits, run the relevant Scoop validation available in your environment and record exact commands and results; this repository does not document a separate automated test suite.

Validate JSON and confirm download URLs, executable paths, SHA-256 values, version checks and automatic update URLs refer to the intended release. Include installation or upgrade observations when available. Do not rewrite checksums merely to make a failed download pass. A checksum matches bytes; it does not independently establish source provenance or successful operation on every supported system. Preserve existing upstream release and signing responsibilities.

## Pull requests

Create a focused branch from the current `main` branch and submit a pull request to this repository. Link the relevant issue or existing project task, explain the resulting behaviour, and update affected examples and documentation. Keep unrelated changes in separate pull requests.

Report executed commands, outcomes and the commit they validate. Identify unavailable checks and remaining limitations explicitly. Follow the repository's existing review and automated-check requirements; retain required gates and current ownership. Address findings and verify the final head before integration. Repository changes do not themselves authorise a release or external operational action.

## Security, rights and conduct

Follow the [security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Use private vulnerability reporting if available; otherwise request a private contact without publishing vulnerability details. Keep credentials, personal information and restricted source material out of issues, fixtures, logs and artifacts.

Preserve existing attribution and third-party terms. This guide does not grant a licence; clarify any unclear redistribution rights before contributing external material. Follow the [code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md) and keep technical discussions respectful.

## Basis for this guide

This guide follows [GitHub's contribution-guideline guidance](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors) and the contribution-process and testing principles in [OpenSSF Best Practices](https://www.bestpractices.dev/en/criteria). It does not assert certification.
