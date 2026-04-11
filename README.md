### Hi there 👋

I'm a DevOps/SRE engineer focused on building high-performance distributed systems.

#### 🔧 What I work with

**Infrastructure:** Kubernetes, Istio, Docker, Terraform<br/>
**Monitoring:** Prometheus, Grafana, Thanos, ClickHouse<br/>
**Cloud:** AWS<br/>
**Languages:** Rust, Go, TypeScript, Python

---

#### ⛓️ Featured Project: [QFC Blockchain](https://github.com/qfc-network)

A custom Layer 1 blockchain with Proof-of-Contribution consensus, DeFi, NFT marketplace, and full wallet ecosystem.

```mermaid
graph LR
    Wallet[Wallet] -->|RPC| Node[QFC Node]
    Explorer[Explorer] -->|API| Node
    Node -->|P2P libp2p| Node2[QFC Node]
    Node --> Storage[(RocksDB)]
    DeFi[DEX / DeFi] -->|Contracts| Node
    NFT[NFT Marketplace] -->|Contracts| Node
```

**Core:** [qfc-core](https://github.com/qfc-network/qfc-core) — Rust blockchain node with Blake3 PoW, Merkle Patricia Trie, Ed25519/VRF cryptography, libp2p networking<br/>
**Ecosystem:** Explorer, DEX, NFT marketplace, wallet (desktop + mobile), faucet, AI inference router, SDK (JS/Python), VS Code extension<br/>
**34 repositories** covering the full blockchain stack

**Tech stack:** Rust, RocksDB, libp2p, Blake3, Ed25519, React, TypeScript, Solidity

---

#### 🛰️ Featured Project: [Sigma](https://github.com/lai3d/sigma)

Lightweight VPS fleet management platform — track instances across dozens of cloud providers, manage IP addresses, and monitor with Prometheus/Grafana.

```mermaid
graph LR
    Web[React UI] -->|API| Server[Rust + Axum]
    Server --> PG[(PostgreSQL)]
    Agent1[sigma-agent<br/>VPS-1] -->|heartbeat| Server
    Agent2[sigma-agent<br/>VPS-N] -->|heartbeat| Server
    Prom[Prometheus] -.->|scrape| Agent1
    Prom -.->|scrape| Agent2
```

**Components:** sigma-api (Rust/Axum), sigma-web (React), sigma-agent, sigma-probe, sigma-cli<br/>
**Tech stack:** Rust, Axum, PostgreSQL, Redis, Prometheus, Grafana, Thanos, React, Docker, K8s

---

#### 🚀 Featured Project: [EdgeFlow CDN](https://github.com/EdgeFlowCDN)

A self-built content delivery network with edge caching, intelligent scheduling, and security.

```mermaid
graph LR
    User --> Scheduler[DNS Scheduler]
    Scheduler --> Edge[Edge Node]
    Edge --> Origin[Origin]
    Console[Admin UI] -->|REST API| Control[Control Plane]
    Control -->|gRPC| Edge
```

**Highlights:**
- **Edge Node** ([cdn-edge](https://github.com/EdgeFlowCDN/cdn-edge)) — 32K QPS caching proxy with two-tier LRU cache, WAF, HTTP/3, Gzip/Brotli, WebSocket, image optimization
- **Control Plane** ([cdn-control](https://github.com/EdgeFlowCDN/cdn-control)) — REST API + gRPC config sync, JWT + TOTP 2FA, audit logging
- **Scheduler** ([cdn-scheduler](https://github.com/EdgeFlowCDN/cdn-scheduler)) — DNS + HTTP 302 routing with GeoIP, health checks, load-weighted selection
- **Admin Console** ([cdn-console](https://github.com/EdgeFlowCDN/cdn-console)) — React + TypeScript + Ant Design dashboard
- **8 repositories** covering edge proxy, control plane, scheduler, console, CLI, deployment, Terraform, design docs

**Tech stack:** Go, gRPC, PostgreSQL, Redis, ClickHouse, Prometheus, React, Docker, K8s

---

#### 🧠 Featured Project: [MerlionOS](https://github.com/MerlionOS)

A bare-metal operating system purpose-built for LLM inference — zero overhead, maximum throughput.

```mermaid
graph LR
    App[LLM Inference] --> Kernel[merlion-kernel]
    Kernel --> GPU[GPU Direct Access]
    Kernel --> Mem[Memory Manager]
    Go[Go Programs] -->|go-merlionos| Kernel
    Rust[Rust Programs] -->|libmerlion| Kernel
    C[C/C++ Programs] -->|musl-merlionos| Kernel
```

**Core:** [merlion-kernel](https://github.com/MerlionOS/merlion-kernel) — Custom kernel with GPU-first scheduling, zero-copy memory management<br/>
**Language support:** Go ([go-merlionos](https://github.com/MerlionOS/go-merlionos)), Rust ([libmerlion](https://github.com/MerlionOS/libmerlion)), C/C++ ([musl-merlionos](https://github.com/MerlionOS/musl-merlionos))<br/>
**Inference:** [merlion-infer](https://github.com/MerlionOS/merlion-infer) — Bare-metal LLM inference engine<br/>
**Zig port:** [merlionos-zig](https://github.com/MerlionOS/merlionos-zig) — Clean reimplementation in Zig<br/>
**Try it:** [Playground](https://github.com/MerlionOS/merlionos-playground)

**Tech stack:** Rust, Zig, Assembly, C, Go, GPU/CUDA
