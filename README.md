### Virgile de La Rochefoucauld

AI Research Engineer — autonomous deliberation for multi-robot systems.
PhD 2025, LAAS-CNRS × Osaka University. Currently technical lead, autonomy, at Safran Electronics & Defense.

My thesis built **AMA**: a centralised symbolic planner paired with a distributed, temporally
supervised execution system for robot teams operating across air, surface and water.
Everything below is independent research on the same question : *how does an smart autonomous
systems decide what to do next, and how do you check the decision while acting on it?*

---

#### Verified deliberation

| | |
|---|---|
| **[ama-planning](https://github.com/ViDLR/ama-planning)** | Reference implementation of the thesis architecture. AMA-Plan decomposes a mission into sequentially linked sub-problems; AMA-Exec dispatches over an extended Simple Temporal Network and survives desynchronisation and robot failure. Reproduces the IEEE Access figures. |
| **[stn-exec](https://github.com/ViDLR/stn-exec)** | Simple Temporal Networks with uncertainty — propagation, dynamic controllability, and an execution dispatcher that cleanly separates the temporal model from the robot interface. |
| **[symbolic-mission-planner](https://github.com/ViDLR/symbolic-mission-planner)** | Natural language → mission spec. Prolog checks the rules and explains violations, CP-SAT allocates and schedules, Prolog re-verifies the result with no shared state. The model never writes the plan; the solver never certifies itself. |

#### Learning under constraints

| | |
|---|---|
| **[verified-options](https://github.com/ViDLR/verified-options)** | Hierarchical RL options with symbolic preconditions and verified effects. A failed postcondition returns control upward and triggers replanning. Headline metric: catastrophic-option rate with and without the gate, on MiniGrid and PyBullet. |
| **[odd-guardian](https://github.com/ViDLR/odd-guardian)** | Safety requirements and operational design domain as Signal Temporal Logic, validated against one concrete example before formalisation, then falsified by search in simulation. Reports the violating trace, not a verdict. |

#### Deliberation beyond robotics

| | |
|---|---|
| **[ask-before-build](https://github.com/ViDLR/ask-before-build)** → **[donewhen](https://github.com/ViDLR/donewhen)** | The same contract AMA-Exec imposes on a robot plan, applied to coding agents: scope the goal before acting, prove the stopping condition before claiming it. Scored on a held-out corpus never used for tuning. |

---

#### Publications

- **A Modular Execution Architecture for Robust Multi-Robot Planning and Acting in Trans-Media Environments** — *IEEE Access*, 2025
- **Solving Multi-Robot Task Allocation and Planning in Trans-media Scenarios** — *IEEE/RSJ IROS*, Abu Dhabi, 2024
- **Planning and Acting in Multi-Environment Aerial, Surface and Aquatic Missions with Multi-Robot Teams** — PhD thesis, Université de Toulouse (INSA) in cotutelle with Osaka University, LAAS-CNRS, 2025

[vidlr.github.io](https://vidlr.github.io) · [LinkedIn](https://www.linkedin.com/in/virgile-de-la-rochefoucauld/) · virgile.dlr@protonmail.com
