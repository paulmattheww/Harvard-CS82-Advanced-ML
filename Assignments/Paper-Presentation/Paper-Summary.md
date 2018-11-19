# Summary of [Relational Inductive Biases, Deep Learning, and Graph Networks](https://arxiv.org/pdf/1806.01261.pdf)

Paul M. Washburn
CSCI E-82 Advanced Machine Learning, Data Mining & Artificial Intelligence
Harvard Extension School, Fall 2018

### Authors:  Pater W. Battaglia, Jessica B. Hamrick, Victor Bapst, Alvaro Sanchez-Gonzalez, Vinicius Zambaldi, Mateusz Malinowski, Andrea Tacchetti, David Raposo, Adam Santoro, Ryan Faulkner, Caglar Gulcehre, Francis Song, Andrew Ballard, Justin Gilmer, George Dahl, Ashish Vaswani, Kelsey Allen, Charles Nash, Victoria Langston, Chris Dyer, Nicolas Heess, Daan Wierstra, Pushmeet Kohli, Matt Botvinick, Oriol Vinyals, Yujia Li, Razvan Pascanu

### Institutions:  DeepMind, Google Brain, Massachussetts Institute of Technology, University of Edinburgh

This recent paper is a bold departure from current topics in machine learning research.  Inspiration for the research was drawn from the fact that "generalizing beyond one [model's] experiences ... remains a formidable challenge for modern AI" -- necessitating an extension of the AI developer's toolbox.  The authors reject what they characterize as a "false choice" between manually engineered models (e.g. if-then type systems) and end-to-end learning systems (e.g. an `sklearn` `Pipeline`), instead opting for a strategy that takes advantage of the two approaches' complementary strengths.  The authors utilize neural network architectures that incorporate the sort of object-based understanding humans have of the world by representing entities and their relationships explicitly.  Introduced is the notion of using *relational inductive biases* within a *graph network* built upon deep learning computational struvtures, supplying a new building block for AI systems.  *Inductive biases* allow learning algorithms to prioritize one solution over another.  This new paradigm enables a structured-yet-flexible approach that takes advantage of established knowledge & rules (e.g. entities of type `animal` must eat) while allowing for the complex & nuianced representations learned in neural networks (e.g. inputting pixels and outputting a classification), paving the way for "more sophisticated, interpretable and flexible patterns of reasoning".  Various deep learning architectures are leveraged & adapted from previous works for use in this approach, including Non-Local Neural Networks (NLNN) and Message-Passing Neural Networks (MPNN).  The three basic design principles in constructing such models include **flexible representations, configurable within-block structure**, and **composable multi-block architectures** are designed to help the graphical representation support combinatorial generalization.  The authors also released an [open-source Python package called `graph_nets`](https://github.com/deepmind/graph_nets) for users to begin experimenting.

Below is the original Abstract from the paper:

```
Abstract
Artificial intelligence (AI) has undergone a renaissance recently, making major progress in
key domains such as vision, language, control, and decision-making. This has been due, in
part, to cheap data and cheap compute resources, which have fit the natural strengths of deep
learning. However, many defining characteristics of human intelligence, which developed under
much different pressures, remain out of reach for current approaches. In particular, generalizing
beyond one’s experiences—a hallmark of human intelligence from infancy—remains a formidable
challenge for modern AI.
The following is part position paper, part review, and part unification. We argue that
combinatorial generalization must be a top priority for AI to achieve human-like abilities, and that
structured representations and computations are key to realizing this objective. Just as biology
uses nature and nurture cooperatively, we reject the false choice between “hand-engineering”
and “end-to-end” learning, and instead advocate for an approach which benefits from their
complementary strengths. We explore how using relational inductive biases within deep learning
architectures can facilitate learning about entities, relations, and rules for composing them. We
present a new building block for the AI toolkit with a strong relational inductive bias—the graph
network—which generalizes and extends various approaches for neural networks that operate
on graphs, and provides a straightforward interface for manipulating structured knowledge and
producing structured behaviors. We discuss how graph networks can support relational reasoning
and combinatorial generalization, laying the foundation for more sophisticated, interpretable,
and flexible patterns of reasoning. As a companion to this paper, we have also released an
open-source software library for building graph networks, with demonstrations of how to use
them in practice.
```
