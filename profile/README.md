# Model Authentication Protocol (MAP)

Welcome to the home of **MAP (Model Authentication Protocol)**. 

As AI agents become more autonomous and deeply integrated into our workflows through the **Model Context Protocol (MCP)**, traditional web-era security methods like OAuth 2.1 introduce heavy friction, constant re-authentications, and a poor experience for both humans and agents. 

**MAP is a purpose-built security tool designed specifically to secure MCP servers.** It bridges the gap between rigorous, least-privilege security and the high-bandwidth, continuous nature of AI agent interactions.

---

### Why MAP?

* **Built for Agents, Not Browsers:** Ditch heavy login loops and browser-based OAuth redirects. MAP uses lightweight cryptographic proofs and intent-bound capabilities tailored to AI workloads.
* **Streamlined Security for MCP Servers:** Secure your MCP endpoints with a dedicated trust layer that handles permissions and identity verification independently without bloating your core data protocol.
* **Frictionless Human-in-the-Loop:** When elevated actions or permissions are needed, MAP triggers quick, seamless device confirmations rather than breaking the agent's flow with recurring token expirations.
* **Granular Least-Privilege Access:** Ensure that agents only access the specific tools and data required for the task at hand—drastically minimizing risks like prompt injection or unauthorized access.

---

### How It Works

> ```
> +-------------+      1. Request Capability      +-------------+
> | AI Agent /  | ------------------------------> | MAP Gateway |
> | MCP Client  | <------------------------------ |             |
> +-------------+     2. Signed Capability Token  +-------------+
>        |                                                |
>        | 3. Invoke Tool w/ Token                        | 4. Quick Human Tap /
>        v                                                v    Biometric Approval
> +-------------------------------------------------------------+
> |                         MCP Server                          |
> +-------------------------------------------------------------+
> ```

1. **Identity & Intent:** When an agent attempts to invoke a tool on an MCP server, it presents a verified workload identity via MAP.
2. **Context Evaluation:** MAP evaluates the request against trust policies and explicit user risk thresholds.
3. **Seamless Approval:** High-privilege actions trigger a lightweight, one-tap micro-prompt to the human user rather than a full re-authentication loop.
4. **Ephemeral Capabilities:** Short-lived, highly scoped capability tokens are issued, expiring automatically the moment the task concludes.

---

### Roadmap & Ecosystem

MAP is designed to be deeply interoperable yet loosely coupled with MCP, making it easy for developers to adopt. We are building SDKs and support across major developer runtimes (including **TypeScript** and **Python**) to make securing your MCP servers plug-and-play.

Join us in building a more secure, streamlined future for human-agent collaboration. Check out our repositories to get started, contribute, or integrate MAP into your next agent project.
