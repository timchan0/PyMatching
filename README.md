# PyMatching with Swim Distance

This repository is a fork from
[this commit](https://github.com/oscarhiggott/PyMatching/tree/a9b8da24833871c7dbe4fa90fc85920b2716c7d1)
of PyMatching.
The swim distance implementation is written by Zihan-Chen,
_not_ me!
I've just tidied it up slightly.

## Local Installation Instructions

Dependencies:

* numpy
* pymatching

The following instructions are taken from https://github.com/Zihan-Chen-PhMA/Cultiv_T_RP2/blob/main/installation_guide.md
but with a bug fix.
Install the customized `pymatching` package in editable mode:
1. Git clone the customized version:
    ```
    git clone --recursive https://github.com/timchan0/PyMatching
    ```
2. Go to the cloned PyMatching folder, then:
    ```
    pip install -e .
    ```

## Usage

See `SO_example/mwe.ipynb`.

## Zihan-Chen's Description
The soft-output method in [arXiv:2405.07433](https://arxiv.org/abs/2405.07433) by Meister et al. serves a similar purpose as the complementary gap method in 
[arXiv:2312.04522](https://arxiv.org/abs/2312.04522) but is more versatile since the soft-output method does not have a hard requirement on the boundary condition of the surface codes or decoding 
graphs. Following [this StackExchange post](https://quantumcomputing.stackexchange.com/questions/35572/how-to-force-pymatching-into-the-opposite-equivalence-class), 
the soft-output method can be implemented on the sparse blossom algorithm so that for each decoding shot, a soft output (or 
perhaps a few soft outputs) is calculated based on the internal variables (graph_fill_regions) created during the decoding process. See folder [SO_example](https://github.com/timchan0/PyMatching/tree/master/SO_example) for an 
example of how to obtain soft output when decoding SE circuits on rotated surface codes. 