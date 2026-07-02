# Encryption (encryption)
An index and topic collection covering encryption services, key management systems (KMS), hardware security modules (HSM), envelope encryption, end-to-end encryption SDKs, certificate management, and code/data signing. This topic gathers the cryptographic primitives, managed services, and open-source libraries that protect data at rest and in transit across cloud, mobile, web, and supply-chain workloads. It includes managed KMS offerings (AWS KMS, Google Cloud KMS, Azure Key Vault), HSM and enterprise key management platforms, secrets and configuration encryption tooling (HashiCorp Vault, Doppler, SOPS), code- and artifact-signing infrastructure (Sigstore, Cosign, Notary, TUF), end-to-end encrypted messaging protocols (Signal, Matrix), and certificate authority APIs (Let's Encrypt, DigiCert, Amazon Private CA). Distinct from the broader Security topic, this collection focuses specifically on cryptography, keys, certificates, and signing.

**URL:** [https://apievangelist.com](https://apievangelist.com)

## Tags:

 - Encryption, KMS, HSM, Cryptography, Key Management, Certificate Management, Code Signing, End-to-End Encryption

## Timestamps

- **Created:** 2026-05-19
- **Modified:** 2026-05-19

## Common Properties

- [Portal](https://apievangelist.com)
- [GitHubOrganization](https://github.com/api-evangelist)
- [JSONSchema - Customer Master Key Schema](https://raw.githubusercontent.com/api-evangelist/encryption/refs/heads/main/json-schema/encryption-cmk-schema.json)
- [JSONSchema - Encrypt Request Schema](https://raw.githubusercontent.com/api-evangelist/encryption/refs/heads/main/json-schema/encryption-encrypt-request-schema.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/encryption/refs/heads/main/json-ld/encryption-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/encryption/refs/heads/main/vocabulary/encryption-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| Managed Key Management Services | Cloud KMS offerings like AWS KMS, Google Cloud KMS, and Azure Key Vault provide managed creation, rotation, and lifecycle of cryptographic keys with hardware-backed protection and IAM-controlled access. |
| Hardware Security Module APIs | Network-attached HSMs and HSM-backed services such as AWS CloudHSM, Azure Dedicated HSM, and Google Cloud HSM expose tamper-resistant cryptographic operations through PKCS#11 and REST APIs. |
| Envelope Encryption Patterns | Envelope encryption wraps data encryption keys (DEKs) with key encryption keys (KEKs) stored in a KMS, enabling scalable encryption of large data sets while centralizing key control. |
| End-to-End Encryption Protocols | Open protocols like Signal, Matrix Olm/Megolm, and MLS provide forward-secret, deniable end-to-end encryption for messaging, calling, and collaboration applications. |
| Certificate Lifecycle Automation | ACME-based services like Let's Encrypt, alongside enterprise CAs like DigiCert and Amazon Private CA, automate issuance, renewal, and revocation of TLS and code-signing certificates. |
| Code and Artifact Signing | Sigstore, Cosign, Notary, and TUF provide keyless and key-based signing of container images, binaries, and software packages with transparency-log-backed verification. |
| Secrets and Configuration Encryption | Tools like HashiCorp Vault, Doppler, and SOPS encrypt secrets, environment variables, and configuration files in transit and at rest, integrating with KMS providers and CI/CD pipelines. |
| Open-Source Cryptographic Libraries | Libraries like Google Tink, libsodium, OpenSSL, and BoringSSL provide misuse-resistant primitives for symmetric, asymmetric, AEAD, hashing, and digital signature operations. |

## Use Cases

| Name | Description |
|------|-------------|
| Encrypting Data at Rest in the Cloud | Applications use cloud KMS APIs to encrypt database fields, S3 objects, and disk volumes with envelope encryption, ensuring keys never leave a managed boundary while data ciphertext can be stored anywhere. |
| TLS Termination and Certificate Renewal | Web platforms automate TLS certificate provisioning and rotation through ACME (Let's Encrypt) or enterprise CA APIs (DigiCert, Amazon Private CA), keeping in-transit encryption healthy without manual operations. |
| Software Supply Chain Signing | Build pipelines sign container images and binaries with Sigstore/Cosign, anchoring artifacts to transparency logs so downstream consumers can verify provenance before deploying. |
| End-to-End Encrypted Messaging and Collaboration | Messaging applications integrate Signal protocol, Matrix Olm/Megolm, or MLS to provide forward-secret encryption where neither the service operator nor an attacker can read message content. |
| Secrets Management for CI/CD | HashiCorp Vault, Doppler, and SOPS encrypt secrets used across CI/CD pipelines, source control, and runtime environments, integrating with cloud KMS for sealed storage and audit logging. |
| Tokenization and Payment Cryptography | Payment processors and PCI workloads use services like AWS Payment Cryptography and Apple Pay tokenization to perform PIN translation, card encryption, and EMV operations under FIPS-validated HSMs. |
| Workload Identity and Zero-Trust Cryptography | SPIFFE/SPIRE issue short-lived, cryptographically verifiable workload identities (SVIDs) so services can mutually authenticate without long-lived secrets across multi-cloud environments. |

## Integrations

| Name | Description |
|------|-------------|
| AWS KMS | Managed key creation, envelope encryption, and HSM-backed cryptographic operations integrated across AWS services and accessible via SDK and REST APIs. |
| Google Cloud KMS | Multi-region, software- and HSM-backed key management for envelope encryption and signing across GCP services and external KMS scenarios. |
| Azure Key Vault | Centralized key, secret, and certificate management with HSM-backed key protection and tight integration into Azure services and Entra ID. |
| HashiCorp Vault | Open-source secrets management with a Transit engine for encryption-as-a-service, PKI engine for certificate issuance, and KMIP server for HSM integration. |
| Sigstore | Free, keyless software signing infrastructure built around Fulcio (CA), Rekor (transparency log), and Cosign (signing CLI), now broadly used for OSS supply chain integrity. |
| Let's Encrypt | Free, automated ACME-based certificate authority issuing billions of TLS certificates that underpin in-transit encryption for the public web. |
| Tink | Google's misuse-resistant cryptography library providing AEAD, MAC, hybrid encryption, and signature primitives with pluggable KMS backends. |
| Signal Protocol | Forward-secret, end-to-end encryption protocol used by Signal, WhatsApp, and others, providing double-ratchet key derivation and prekey-based async messaging. |

## Artifacts

Machine-readable API specifications organized by format.

### JSON Schema

- [Customer Master Key Schema](json-schema/encryption-cmk-schema.json)
- [Encrypt Request Schema](json-schema/encryption-encrypt-request-schema.json)

### JSON Structure

- [Customer Master Key Structure](json-structure/encryption-cmk-structure.json)
- [Encrypt Request Structure](json-structure/encryption-encrypt-request-structure.json)

### JSON-LD

- [Encryption Context](json-ld/encryption-context.jsonld)

## Vocabulary

- [Encryption Vocabulary](vocabulary/encryption-vocabulary.yaml) — Unified taxonomy mapping resources, actions, workflows, and personas across KMS, HSM, certificate management, end-to-end encryption, and code signing.

## Network

This index references the following encryption, KMS, HSM, certificate, and signing repositories:

- [Amazon KMS](https://github.com/api-evangelist/amazon-kms)
- [Amazon Payment Cryptography](https://github.com/api-evangelist/amazon-payment-cryptography)
- [Amazon Private CA](https://github.com/api-evangelist/amazon-private-ca)
- [Amazon Signer](https://github.com/api-evangelist/amazon-signer)
- [Apple Pay](https://github.com/api-evangelist/apple-pay)
- [Azure Key Vault](https://github.com/api-evangelist/azure-key-vault)
- [Cosign](https://github.com/api-evangelist/cosign)
- [DigiCert](https://github.com/api-evangelist/digicert)
- [Doppler](https://github.com/api-evangelist/doppler)
- [Google Cloud KMS](https://github.com/api-evangelist/google-cloud-kms)
- [Google Cloud Secret Manager](https://github.com/api-evangelist/google-cloud-secret-manager)
- [HashiCorp Vault](https://github.com/api-evangelist/hashicorp-vault)
- [Let's Encrypt](https://github.com/api-evangelist/lets-encrypt)
- [Lit Protocol](https://github.com/api-evangelist/lit-protocol)
- [Matrix](https://github.com/api-evangelist/matrix)
- [Notary Project](https://github.com/api-evangelist/notary)
- [OpenSSF](https://github.com/api-evangelist/openssf)
- [OpenWallet Foundation](https://github.com/api-evangelist/openwallet-foundation)
- [Signal](https://github.com/api-evangelist/signal)
- [Sigstore](https://github.com/api-evangelist/sigstore)
- [SOPS](https://github.com/api-evangelist/sops)
- [SPIFFE](https://github.com/api-evangelist/spiffe)
- [SSH](https://github.com/api-evangelist/ssh)
- [Symantec](https://github.com/api-evangelist/symantec)
- [Symphony](https://github.com/api-evangelist/symphony)
- [Tink](https://github.com/api-evangelist/tink)
- [The Update Framework](https://github.com/api-evangelist/tuf)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
