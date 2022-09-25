# Soft Actor-Critic for logic

(Forked from https://github.com/toshikwa/soft-actor-critic.pytorch)

A PyTorch implementation of Soft Actor-Critic[[1,2]](#references) with n-step rewards and prioritized experience replay[[3]](#references).

## Requirements

You can install liblaries using `pip install -r requirements.txt` except `mujoco_py`.

Note that you need a licence to install `mujoco_py`. For installation, please follow instructions [here](https://github.com/openai/mujoco-py).

## Examples
You can train Soft Actor-Critic agent like this example [here](https://github.com/ku2482/soft-actor-critic.pytorch/blob/master/code/main.py).

```
python code/main.py \
[--env_id str(default HalfCheetah-v2)] \
[--cuda (optional)] \
[--seed int(default 0)]
```

If you want to use n-step rewards and prioritized experience replay, set `multi_step=5` and `per=True` in configs.

## References
[[1]](https://arxiv.org/abs/1801.01290) Haarnoja, Tuomas, et al. "Soft actor-critic: Off-policy maximum entropy deep reinforcement learning with a stochastic actor." arXiv preprint arXiv:1801.01290 (2018).

[[2]](https://arxiv.org/abs/1812.05905) Haarnoja, Tuomas, et al. "Soft actor-critic algorithms and applications." arXiv preprint arXiv:1812.05905 (2018).

[[3]](https://arxiv.org/abs/1511.05952) Schaul, Tom, et al. "Prioritized experience replay." arXiv preprint arXiv:1511.05952 (2015).
