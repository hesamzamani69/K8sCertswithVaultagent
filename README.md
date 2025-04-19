# K8sCertswithVaultagent

# 🔐 Vault Agent TLS Certificate Sidecar for Kubernetes

A production-ready example for managing short-lived TLS certificates in Kubernetes Pods using **HashiCorp Vault**, **Vault Agent**, **Kubernetes Auth**, and the **Sidecar pattern**.

> 📘 Designed for cloud-native environments that require automated, auditable, and secure certificate lifecycle management.

---

## ✨ Features

- ⚡ Automated issuance and rotation of short-lived TLS certificates
- 🔒 Zero-touch injection via Vault Agent as a sidecar
- 🧠 Role-based access using Kubernetes ServiceAccounts
- 📜 Template-based cert rendering with live reload support
- 🔍 Vault audit logs for full traceability
- 🚀 Ready-to-deploy with Helm & example manifests

---

## 📦 Project Structure


---

## 🚀 Quickstart

1. **Deploy Vault** with Kubernetes Auth and PKI enabled (use `scripts/setup-pki.sh`)
2. **Install the Helm chart**:

   ```bash
   helm install vault-agent ./charts/vault-agent

🛠 Requirements
Kubernetes v1.20+

Vault 1.12+ with pki and kubernetes auth enabled

Helm 3.x


📁 What’s Inside?
✅ Vault Agent HCL config with auto_auth and template

✅ Cert rendering via pki_int/issue/<role>

✅ Live reloading support (command = "kill -HUP" on cert change)

✅ Clean service separation between application and agent

✅ Short-lived certs with 24h TTL



🔐 Security Practices
Certificates and private keys never touch Git or disk long-term

Pods get certs only if authorized via ServiceAccount and Namespace

Tokens are ephemeral and scoped

Vault audit logs provide fine-grained visibility
