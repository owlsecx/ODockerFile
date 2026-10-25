# 🦉 ODockerFile

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ODockerFile** — Dockerfile & Compose Security Linter

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ODockerFile — Dockerfile & Compose Security Linter. It provides full Dockerfile parser — line continuations, escape directive, exec/shell form, flags, heredocs, stages, ARG/ENV substitution, inline suppressions. Built-in demo/self-test paths and severity gates help validate detections without touching production when those flags are used.

---

## ✨ Features

- Full Dockerfile parser — line continuations, escape directive, exec/shell form, flags, heredocs, stages, ARG/ENV substitution, inline suppressions
- Stdlib-only YAML subset parser for docker-compose (block/flow maps & lists, anchors, merge keys, scalars)
- 50+ Dockerfile rules — mutable tags, root user, ADD remote URLs, secrets in ENV/ARG, curl|bash, apt / apk / yum / pip hygiene, TLS-verify bypass, chmod 777, setuid
- 30+ Compose rules — privileged, cap_add, host network / pid / ipc / uts / userns, docker.sock & host-root binds, seccomp/apparmor unconfined, limits, read-only rootfs
- Every rule mapped to CIS Docker Benchmark + CWE with severity, rationale and concrete remediation
- Directory tree discovery (Dockerfile*, Containerfile, *.dockerfile, docker-compose*.yml, compose*.yaml)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ODockerFile                                     # interactive menu
./ODockerFile --scan -r /path/to/root
./ODockerFile --demo
./ODockerFile --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
