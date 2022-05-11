# Pytorch Implementation of Physics-informed Neural Networks (PINN)

In this repo, the both of discrete-time and continuous-time Burgers equation for inference and parameters identification are implemented.

## Attribute

**Original Work**: *Maziar Raissi, Paris Perdikaris, and George Em Karniadakis*

**Github Repo** : <https://github.com/maziarraissi/PINNs>

@article{raissi2017physicsI,
  title={Physics Informed Deep Learning (Part I): Data-driven Solutions of Nonlinear Partial Differential Equations},
  author={Raissi, Maziar and Perdikaris, Paris and Karniadakis, George Em},
  journal={arXiv preprint arXiv:1711.10561},
  year={2017}
}

@article{raissi2017physicsII,
  title={Physics Informed Deep Learning (Part II): Data-driven Discovery of Nonlinear Partial Differential Equations},
  author={Raissi, Maziar and Perdikaris, Paris and Karniadakis, George Em},
  journal={arXiv preprint arXiv:1711.10566},
  year={2017}
}

Also, this [repo](https://github.com/jayroxis/PINNs/blob/master/README.md#attribute) is a good reference.

## Some confusion points

For discrete-time case, what you need is a Jocobian matrix. However,  ```torch.autograd.grad``` returns vector-Jacobian product. You need one more step to recover the jocobian matrix. I added some notes in my code.
