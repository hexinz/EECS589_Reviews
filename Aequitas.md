# [Aequitas: Admission Control for Performance-Critical RPCs in Datacenters](https://yiwenzhang92.github.io/assets/docs/aequitas-sigcomm22.pdf)

###### Hexin Zhang (hexinz@umich.edu)

---
### Three Important Contributions
<!-- -List at least three important contributions of this paper. -->
- The paper proposed Aequitas, a admission control system that provides service-level objectives (SLOs) for performance-critical Remote Procedure Calls (PC RPCs) regardless of their size, even when network demand is 10 times beyond provisioned capacity (at the 99.9th-p RNL).
- Realied cluster-wide predictable latency performance.
- Hosts can make local decisionis to admit or downgrade QoS for an RPC.

### The Methodology

<!-- -Describe the methodology used in the paper and how you would use it for other studies. -->
- 1:1 align the PC, non-critical (NC), and best-effort (BE) RPCs to high/medium/low-weight network QoS queues by encoding the QoS in the packet’s DSCP header field; use Weighted Fair Queue (WFQ) in switches which has delay bounds.
- Employ a distributed admission control scheme to manage the traffic at QoS level; individually measure RPC Network-Latency (RNL); downgrade excess traffic to low-weight network QoS queue to meet SLOs for the higher QoS classes.

### The Inherent Assumption or the Model
<!-- -Describe the inherent assumption or the model used in the paper if any. -->
- Assumption 1: when the demand for each QoS class exceeds its minimum guaranteed rate, the QoS-share thresholds for priority inversion are a function of QoS weights
- Assumption 2: while increasing QoS weight helps admit more QoS traffic with zero delay, beyond QoS-share exceeding some number, delay is independent of QoS weights.

### Flaws
<!-- -Describe any flaws in the paper. The flaws can be any simplications made that may significantly affect the results. Propose any future work or follow-up studies. -->
??
