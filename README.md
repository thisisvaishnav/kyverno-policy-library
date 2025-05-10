# Kyverno Policy Repository

This repository contains a collection of Kyverno policies designed for Kubernetes security and configuration management. Kyverno is a Kubernetes native policy engine that allows you to validate, mutate, and generate configurations dynamically.

## 📌 **Project Structure**

```
├── policies
│   ├── validation
│   ├── mutation
│   └── generation
├── examples
│   ├── validation-examples
│   ├── mutation-examples
│   └── generation-examples
├── scripts
│   └── deploy.sh
├── README.md
└── LICENSE
```

* **policies**: Contains all Kyverno policy YAML files categorized into validation, mutation, and generation.
* **examples**: Usage examples for each policy type to test and understand functionality.
* **scripts**: Deployment and helper scripts for easier integration.

---

## 🚀 **Getting Started**

### Prerequisites

* Kubernetes Cluster (Minikube, Kind, EKS, etc.)
* [Kyverno CLI](https://kyverno.io/docs/kyverno-cli/) for local testing

### Installation

To install Kyverno in your cluster:

```sh
kubectl apply -f https://raw.githubusercontent.com/kyverno/kyverno/main/config/install.yaml
```

Verify the installation:

```sh
kubectl get pods -n kyverno
```

---

## 🔎 **Usage**

Apply a policy to your cluster:

```sh
kubectl apply -f policies/validation/validate-resource-limits.yaml
```

Test a policy locally using Kyverno CLI:

```sh
kyverno apply policies/validation/validate-resource-limits.yaml --resource examples/validation-examples/deployment.yaml
```

---

## 🤝 **Contributing**

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes and commit (`git commit -m 'Add new policy'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a Pull Request

---

## 🛡️ **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 **Contact**

For any questions or suggestions, feel free to reach out or open an issue.
