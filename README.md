# Artifacts

**This repo is under construction. Please continue to use
[k8s.io/k8s.io][k/k8s.io] until this migration is officially announced.**

The artifacts repo ([k8s.io/artifacts][k/artifacts]) stores configuration files
for the Kubernetes Community's artifact promoters:

- [`cip` (container image promoter)][cip repo]
- [`kpromo` (file promoter)][kpromo]

Configurations are organized primarily in two directories:

- `registries/` (configurations for image/registry promotion)
- `stores/` (configurations for file/object store promotion)

A snippet of the repo layout:

```console
├── registries
│   └── k8s.gcr.io                          # Production container registry
│       ├── config                          # Registry (GCR) promoter configurations
│       │   ├── k8s-staging-releng
│       │   │   └── promoter-manifest.yaml
│       │   └── OWNERS
│       └── images                          # Image manifests
│           └── k8s-staging-releng
│               └── OWNERS
└── stores
    └── artifacts.k8s.io                    # Production object store
        ├── config                          # Object store (GCS) promoter configurations
        │   ├── k8s-staging-releng
        │   │   └── promoter-manifest.yaml
        │   └── OWNERS
        └── files                           # File manifests
            └── k8s-staging-releng
                └── OWNERS
```

## Resources

- [Managing container registries](https://git.k8s.io/k8s.io/k8s.gcr.io)
- [Image promoter KEP (1734)](https://git.k8s.io/enhancements/keps/sig-release/1734-k8s-image-promoter)
- [Artifact management KEP (1732)](https://git.k8s.io/enhancements/keps/sig-release/1732-artifact-management)

## Community, discussion, contribution, and support

Learn how to engage with the Kubernetes community on the [community page](http://kubernetes.io/community/).

You can reach the maintainers of this project at:

- [Slack (`#release-management`)](https://kubernetes.slack.com/archives/CJH2GBF7Y)
- [Release Managers mailing list](https://groups.google.com/a/kubernetes.io/g/release-managers)

Extended contact information can be found [here](https://git.k8s.io/sig-release/release-managers.md).

### Code of conduct

Participation in the Kubernetes community is governed by the [Kubernetes Code of Conduct](code-of-conduct.md).

[cip repo]: https://sigs.k8s.io/k8s-container-image-promoter
[k/artifacts]: https://git.k8s.io/artifacts
[k/k8s.io]: https://git.k8s.io/k8s.io
[kpromo]: https://git.k8s.io/release/cmd/kpromo/README.md
