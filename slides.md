---
theme: ./slidev-theme-cscs
---

# Accessing Resources on Clariden

<br>

## Slurm, VS Code and Docs

<br>

Ben Cumming

bcumming.github.io/ml-mentors

---
layout: two-cols
layoutClass: gap-2
---

# Slurm

What is Slurm

::right::

```
Basic slurm examples
```

---

# Slurm: interactive sessions

---

# Slurm: allocating GPUs

---

# CSCS Documentation

[`docs.cscs.ch`](https://docs.cscs.ch) is a good starting point for information:
* [PyTorch](https://docs.cscs.ch/software/ml/pytorch/)
* [Jupyter](https://docs.cscs.ch/access/jupyterlab)
* [VS Code](https://docs.cscs.ch/access/vscode)
* [ML Platform](https://docs.cscs.ch/platforms/mlp)

<br>

Ideal world: all questions are answered by a link to the docs

* Let us know if something is missing/unclear/wrong

---
layout: two-cols
layoutClass: gap-2
---

# VS Code

VS Code ([`docs.cscs.ch/access/vscode`](https://docs.cscs.ch/access/vscode)) provides a familiar **IDE experience on Alps** using **remote development** features
1. launches a VS Code server on the remote system
2. connects it to the IDE running on your laptop

<br>

**The catch: the server must be started inside the target environment**

We want to run in our container on a compute node

::right::

Using remote SSH is the easiest way to connect

<img src="./images/vscode-ssh-clariden.png" class="h-60" alt="Alt text for the image">

❌ unfortunately this doesn't work because the server:
* is running on a login node
* is running bare metal

---
layout: two-cols
layoutClass: gap-2
---

# VS Code: use tunnels

To use VS Code on a compute node with a container environment we have to first start the environment that we want to run in on a compute node, and connect to it from VS Code.

**Step 1**: Set up VS Code on your laptop

* Install VS Code on your laptop
* Sign in to GitHub in VS Code
* Install the Tunnels VS Code extension

::right::

**Step 2**:
Install the `code` CLI tool on Clariden. See the [CSCS docs](https://docs.cscs.ch/access/vscode/#installing-the-server).

**Step 3**:
Start the tunnel and connect to VS Code

1. Start a job with the container environment you plan to use
1. Start a tunnel
1. Authenticate on the web
1. connect VS Code on laptop to the tunnel

The CSCS docs have a detailed [step by step instructions](https://docs.cscs.ch/access/vscode/#flexible-method-remote-server).

---


## Questions


