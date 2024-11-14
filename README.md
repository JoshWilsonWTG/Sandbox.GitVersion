# Sandbox.GitVersion
This repo is intended to serve as an example of the use of [GitVersion](https://gitversion.net/). You can install GitVersion as a [Chocolatey package](https://community.chocolatey.org/packages/GitVersion.Portable).

## Example operation with GitVersion
```mermaid
gitGraph:
    commit id: "0.1.0" tag: "0.1.0"
    branch feature/WI00111111 order: 1
    checkout feature/WI00111111
    commit id: "branch: 0.2.0-111111.0"
    commit id: "0.2.0-111111.1"
    commit id: "0.2.0-111111.2"
    checkout main
    merge feature/WI00111111
    commit id: "merge: 0.2.0-alpha.1"
    branch feature/WI00222222 order: 2
    checkout feature/WI00222222
    commit id: "branch: 0.2.0-222222.1"
    commit id: "0.2.0-222222.2"
    checkout main
    merge feature/WI00222222
    commit id: "0.2.0" tag: "0.2.0"
    branch release/0.2.x order: 5
    checkout release/0.2.x
    commit id: "branch: 0.2.1-beta.0"
    branch feature/WI00444444 order: 4
    checkout feature/WI00444444
    commit id: "branch: 0.2.1-444444.0"
    commit id: "0.2.1-444444.1"
    commit id: "0.2.1-444444.2"
    checkout release/0.2.x
    merge feature/WI00444444
    commit id: "merge: 0.2.1-beta.1"
    checkout main
    branch feature/WI00333333 order: 3
    checkout feature/WI00333333
    commit id: "branch: 0.3.0-333333.0"
    commit id: "0.3.0-333333.1"
    commit id: "0.3.0-333333.2"
    checkout main
    merge feature/WI00333333
    commit id: "merge: 0.3.0-alpha.1"
```