## Sybil Risk and XEQM's Mitigation Model

### The perceived or real problem

A common concern with any Proof-of-Stake service-node network is the possibility of a Sybil attack. In this context, a Sybil attack means one actor operates many nodes under different identities in order to gain disproportionate influence over the network.

For XEQM, this concern is reasonable to discuss openly. The migration created a known starting supply, but it also showed that some holders control large balances and that some balances may have been split across multiple wallets. Wallet splitting is not proof of malicious behavior. Large holders often split funds for security, custody, or operational reasons. However, it does create a real monitoring concern because one actor could potentially attempt to run many nodes while appearing to be multiple independent operators.

### Why XEQM is naturally resistant

XEQM inherits its core service-node security model from Oxen. This means network influence is not based on cheap identities. It requires real collateral.

Each full service node requires 200,000 XEQM, and the operator must personally stake at least 100,000 XEQM. That makes each additional node expensive to operate. A Sybil attacker cannot simply create thousands of identities at no cost. They must acquire, stake, and lock meaningful capital for every node they control.

The 14-day unbonding period also reduces the ability to rapidly move stake in and out of nodes. Together, the stake requirement, operator minimum, contributor limits, and unbonding period create economic friction against fast, low-cost Sybil behavior.

### The solution

XEQM's approach is not to claim Sybil risk is impossible. The stronger and more honest position is that XEQM makes Sybil control expensive, visible, and governable.

The network combines several protections:

1. A high capital requirement per node.
2. A 50% minimum operator stake.
3. A maximum operator fee of 10%, reducing abusive reward capture.
4. Public visibility of service-node registration keys and announced IP addresses.
5. Monitoring of operator concentration.
6. A long-term goal of improving the Nakamoto coefficient as the operator set grows.

This creates a layered defense. Economic cost discourages casual attacks. Public infrastructure data helps reveal concentration patterns. Governance provides a response path if an operator appears to be gaining too much influence.

### Guardrails available in the whitepaper

The whitepaper also includes guardrails that can be invoked if concentration becomes a real threat.

The first guardrail is a governance concentration cap. The whitepaper describes a policy target of approximately 50 identifiable nodes per operator, or about 7% of a 700-node network. If an operator appears to exceed that level, the first step is not punishment. The team can contact the operator and give them an opportunity to voluntarily reduce their node count.

The second guardrail is public identification and governance action for non-compliance. If an operator refuses to reduce concentration, the project can escalate through public disclosure and governance response.

The third guardrail is registration-key blocklisting. The whitepaper states that public keys associated with bad actors or abusive behavior can be added to a governance-managed blocklist that prevents future node registration using those keys.

The fourth guardrail is IP and infrastructure monitoring. Because service nodes must announce their IP addresses, clustering by IP, subnet, hosting provider, datacenter, timing, or behavior can be reviewed for concentration risk.

The fifth guardrail is contributor-slot graph analysis. Even on a privacy-preserving chain, service-node registration and contributor-slot behavior can reveal repeated operational patterns. Shared contributor structures, repeated funding behavior, and related registrations can all help identify hidden concentration.

Finally, the whitepaper delays external oracle activation until the network reaches a stronger decentralization threshold. The target Nakamoto coefficient is 8, and external oracle consumer access does not activate until the network reaches at least 6. This prevents higher-trust oracle functionality from launching before the operator set is sufficiently decentralized.

### Summary

XEQM is resistant to Sybil attacks because influence requires capital, stake must be locked, nodes are publicly observable, and governance has defined tools to respond to concentration. The whitepaper does not pretend the risk is zero. Instead, it acknowledges the risk and establishes practical guardrails that can be invoked if operator concentration becomes a real threat.
