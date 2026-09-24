# TD3 and DDPG Robot Arm Control

A study of continuous-control reinforcement learning for a seven-degree-of-freedom Panda arm in PandaReach. The upstream project compares DDPG and TD3 with hindsight experience replay (HER).

## Task and architecture

An actor selects continuous actions; critic networks estimate their value. TD3 uses twin critics and delayed policy updates. HER relabels achieved goals in past transitions to learn more effectively from sparse-goal episodes.

![Upstream arm animation](https://github.com/kaymen99/Robot-arm-control-with-RL/assets/83681204/224cf960-43d8-4bdc-83be-ac8fe37e5be9)

## Repository map

| Path | Purpose |
| --- | --- |
| `agents/` | DDPG and TD3 agents |
| `utils/networks.py` | Actor and critic networks |
| `replay_memory/` | Experience storage and goal relabeling |
| `training/` | Training scripts for the algorithms |
| `main.py` | Upstream playback example |

## Existing upstream outputs

The [original README](UPSTREAM_README.md) contains the author's training plots and animation. No quantitative success-rate claim or new evaluation is made here. The playback example calls `load_models()`, so it requires compatible model files; their availability is not assumed.

## Source and license

Based on and adapted from [kaymen99/Robot-arm-control-with-RL](https://github.com/kaymen99/Robot-arm-control-with-RL). The original documentation, figures, and [MIT license](LICENSE) are retained. No robot simulation was rerun for this fork.