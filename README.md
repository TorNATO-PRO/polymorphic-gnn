# Detecting Polymorphic Viruses with Graph Neural Networks

## What is a Polymorphic Virus

A [*polymorphic virus*](https://www.kaspersky.com/resource-center/definitions/what-is-a-polymorphic-virus) is a "virus that changes its form each time it inserts itself into another program" [^Bishop].  This can make it problematic to detect, as developing a signature for that virus can be quite difficult if perturbations are present that change the instructions to something similar but different. There are an infinite number of possible ways to write a program to solve a task, and so it is imperative to consider non-conventional means of detecting viruses to defend our computers from adversarial threats.  

## Idea

We can develop a control flow diagram for source code using [CoFlo](http://coflo.sourceforge.net/wordpress/), [StaticFG](https://github.com/coetaur0/staticfg) or something similar, and then convert this into a graph data structure. We can then use a relatively novel technique which has received a lot of attention in recent years - Graph Neural Networks - to classify similarity between graphs and determine whether two programs are the same. In this way, we can determine whether two programs are the same and use this to counter polymorphic viruses, which rely on small changes to a program's source code. It could also be used to determine whether two programs are the same, and so this work would have additional implications in other areas as well outside of cybersecurity. 

## Previous Research

Previous research has been done that is very similar to this idea. To obtain novelty for our idea, we should try to expand on one of the papers that has already done something similar.

1. [Intelligent Malware Detection Based on Graph Convolutional Network](https://link.springer.com/article/10.1007/s11227-021-04020-y)
2. [NF-GNN: Network Flow Graph Neural Networks for Malware Detection and Classification](https://arxiv.org/abs/2103.03939)

There are quite a few ideas mentioned in the conclusion for ideas of future research.

[^Bishop]: @book{Bishop_2005, address={Boston}, title={Introduction to computer security}, ISBN={9780321247445}, callNumber={QA76.9.A25 B563 2005}, publisher={Addison-Wesley}, author={Bishop, Matt}, year={2005} }

