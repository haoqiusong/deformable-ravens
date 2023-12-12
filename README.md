**NOTE**: this code is based heavily on [the Ravens code base from Google][1]
and retains the same license.

# Integration of Embodied AI for Tangle-Free Operation in Robot Vacuums
The main contributions of our paper are as follows: 

- We proposed a novel method to integrate the segmentation and rearrangement of deformable linear objects to identify and move cables.
- We designed rigid reward metrics with comprehensive constraints to meaningfully train our agent in a manner that closely mimics real-world scenarios so that it is able to solve the entanglement problem in reality.
- The results validated the coherence of each aforementioned metric between our theoretical framework, indicating the effectiveness of our method.

| [Installation](#installation) | [Environments and Tasks](#environments-and-tasks) | [Quick Start](#quick-start) | 

----

## Installation

This is how to get the code running on a local machine. First, get conda on the
machine if it isn't there already:

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

Then, create a new Python 3.7 conda environment (e.g., named "py3-defs") and
activate it:

```
conda create -n py3-defs python=3.7
conda activate py3-defs
```

Then install:

```
./install_python_ubuntu.sh
```

## Environments and Tasks

In adapting the original repository to align with our specific task requirements, we made crucial modifications to `defs_cable.py`. These changes focused on adjusting both the parameters representing the radius of the beads and the number of parts.

Furthermore, we undertook modifications in `environment.py` to facilitate the extraction of the robot's position to compute the reward function. Our task-specific reward function comprises three decisions, integrated into the `Task` super-class.

## Quick Start

We provide the following example for users to quickly implement our model.

```bash
# Run with default configurations
python main.py
```

[1]:https://github.com/DanielTakeshi/deformable-ravens
