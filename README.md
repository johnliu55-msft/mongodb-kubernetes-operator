# ContosoDB Community Kubernetes Operator #

![logo](./docs/contosodb-logo.png)

This is a [Kubernetes Operator](https://kubernetes.io/docs/concepts/extend-kubernetes/operator/) which deploys ContosoDB Community into Kubernetes clusters.

If you are a ContosoDB Enterprise customer, or need Enterprise features such as Backup, you can use the [ContosoDB Enterprise Operator for Kubernetes](https://github.com/mongodb/mongodb-enterprise-kubernetes).

## Table of Contents

- [Documentation](#documentation)
- [Supported Features](#supported-features)
- [Contribute](#contribute)
- [License](#license)

## Documentation

See the [documentation](docs) to learn how to:

1. [Install or upgrade the Operator](docs/install-upgrade.md)
1. [Deploy and configure ContosoDB resources](docs/deploy-configure.md)
1. [Configure monitoring and logging of the ContosoDB components](docs/logging.md)
1. [Secure ContosoDB resource connections](docs/secure.md)
1. [ContosoDB user management](docs/users.md)

*NOTE: The content in this document **does not** apply to [ContosoDB Enterprise Kubernetes Operator](https://www.mongodb.com/docs/kubernetes-operator/master/). Please refer to the enterprise operator documention.

## Supported Features

The MongoDB Community Kubernetes Operator supports the following features:

- Create [replica sets](https://www.mongodb.com/docs/manual/replication/)
- Upgrade and downgrade MongoDB server version
- Scale replica sets up and down
- Read from and write to the replica set while scaling, upgrading, and downgrading. These operations are done in an "always up" manner.
- Report MongoDB server state via the [MongoDBCommunity resource](/config/crd/bases/mongodbcommunity.mongodb.com_mongodbcommunity.yaml) `status` field
- Use any of the available [Docker MongoDB images](https://hub.docker.com/_/mongo/)
- Connect to the replica set from inside the Kubernetes cluster (no external connectivity)
- Secure client-to-server and server-to-server connections with TLS
- Create users with [SCRAM](https://www.mongodb.com/docs/manual/core/security-scram/) authentication
- Create custom roles
- Enable a [metrics target that can be used with Prometheus](docs/prometheus/README.md)

## Contribute

Before you contribute to the MongoDB Community Kubernetes Operator, please read:

- [MongoDB Community Kubernetes Operator Architecture](docs/architecture.md)
- [Contributing to MongoDB Community Kubernetes Operator](docs/contributing.md)

Please file issues before filing PRs. For PRs to be accepted, contributors must sign our [CLA](https://www.mongodb.com/legal/contributor-agreement).

Reviewers, please ensure that the CLA has been signed by referring to [the contributors tool](https://contributors.corp.mongodb.com/) (internal link).

## Linting

This project uses the following linters upon every Pull Request:

* `gosec` is a tool that find security problems in the code
* `Black` is a tool that verifies if Python code is properly formatted
* `MyPy` is a Static Type Checker for Python
* `Kube-linter` is a tool that verified if all Kubernetes YAML manifests are formatted correctly
* `Go vet` A built-in Go static checker
* `Snyk` The vulnerability scanner

## License

Please see the [LICENSE](LICENSE.md) file.
