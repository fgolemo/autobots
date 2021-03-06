![](overview.png "Nested Set Transformers Overview") 

TL;DR: We propose a framework for obtaining multimodal distributions over future sets of sets based on latent variables and autoregressive modelling of sequences. Based on the framework, we introduce a model architecture called **Nested Set Transformer** that uses multi-head self-attention blocks for social attention between elements, and validate it in the context of motion prediction for autonomous driving (**AutoBot**) where we achieve state-of-the-art results on Nuscenes and urban flow of pedestrian, skaters, and bikes.

## Abstract

Humans have the innate ability to attend to the most relevant actors in their vicinity and can forecast how they may behave in the future. This ability will be crucial for the deployment of safety-critical agents such as robots or vehicles which interact with humans. We propose a theoretical framework for this problem setting based on autoregressively modelling sequences of nested sets, using latent variables to better capture multimodal distributions over future sets of sets. We present a new model architecture which we call a Nested Set Transformer which employs multi-head self-attention blocks over sets of sets that serve as a form of social attention between the elements of the sets at every timestep. Our approach can produce a distribution over future trajectories for all agents under consideration, or focus upon the trajectory of an ego-agent. We validate the Nested Set Transformer for autonomous driving settings which we refer to as ("AutoBot"), where we model the trajectory of an ego-agent based on the sequential observations of key attributes of multiple agents in a scene. AutoBot produces results better than state-of-the-art published prior work on the challenging nuScenes vehicle trajectory modeling benchmark. We also examine the multi-agent prediction version of our model and jointly forecast an ego-agent's future trajectory along with the other agents in the scene. We validate the behavior of our proposed Nested Set Transformer for scene level forecasting with a pedestrian trajectory dataset.

## Paper

The paper can be found on arXiv.org: [https://arxiv.org/abs/2104.00563](https://arxiv.org/abs/2104.00563)

## Code

The full repo will be released soon. 

In the meantime, we provided an easy-to-follow proof of concept including a toy dataset here:

[https://gist.github.com/fgolemo/b762ddc59c83ca19cd15f3767e2c3780](https://gist.github.com/fgolemo/b762ddc59c83ca19cd15f3767e2c3780)

## Examples

<div class="ex-img">
    <img src="./nuscenes-dataset.png" alt="Example: Nuscenes Results">
</div>

On the challenging NuScenes dataset, our model learns plausible paths through intersections. Top row: intersection birdseye view, middle: ground truth input (cyan) and output (magenta) trajectory, bottom: learned plausible paths for the agent.


## Bibtex

    @misc{girgis2021latent,
      title={Latent Variable Nested Set Transformers & AutoBots}, 
      author={Roger Girgis and Florian Golemo and Felipe Codevilla and Jim Aldon D'Souza and Samira Ebrahimi Kahou and Felix Heide and Christopher Pal},
      year={2021},
      eprint={2104.00563},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
    }
