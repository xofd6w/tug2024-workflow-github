# GitHub Workflow template for LaTeX document compilation

This is a template for package maintainers for GitHub-based workflows to compile their documents on GitHub.

It was presented at [TUG 2024](https://www.tug.org/tug2024/).

## Demonstration contents

- Minimal example LaTeX package `mypackage` providing the command `\TheAnswer`. Check `mypacakge.dtx`.
- A test case for the package. Check `testfiles/verify-answer.*`.
- Three kinds of TeXLive setups
  - [`zauguin/setup-texlive-action`](https://github.com/zauguin/install-texlive) - to setup historic TeX Live versions with a defined package list.
  - [`teatimeguest/setup-texlive-action`](https://github.com/teatimeguest/setup-texlive-action) - to setup historic TeX Live versions with a defined package list.
  - [Island of TeX's TeXLive docker image](https://gitlab.com/islandoftex/images/texlive) - to setup a full TeX Live with all available packages.
- How to upload to CTAN using a GitHub action.
  - The action [zauguion/ctan-upload](https://github.com/zauguin/ctan-upload) is used.
  - Requires `ctan.ann` and `.github/workflows/deploy.yaml` to be adapted before use.

To use this with your package, copy `.github/.*` to your repository and adapt the files according to your needs.
We recommend using the [Dependency Printer for TeX Live](https://gitlab.com/islandoftex/texmf/depp) to adapt the file `.github/tl_packages` to contain all required packages.
