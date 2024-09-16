# Doppelganger

A Python package of tools to support population synthesizers. Population synthesizers create make-believe or synthetic households and persons for use in [agent-based models](https://en.wikipedia.org/wiki/Agent-based_model), i.e. models or simulations that attempt to represent the behavior of individual actors or "agents".

> [Merriam Webster's](m-w.com) fourth definition of "synthetic": devised, arranged, or fabricated for special situations to imitate or replace usual realities 

[![Test status](https://circleci.com/gh/sidewalklabs/doppelganger.svg?style=shield&circle-token=67a4ccc244edfded8a475447457f78c7c0d65fdd)](https://circleci.com/gh/sidewalklabs/doppelganger) [![Coverage Status](https://coveralls.io/repos/github/sidewalklabs/doppelganger/badge.svg?t=7Kr9Vl)](https://coveralls.io/github/sidewalklabs/doppelganger)

## Features

Doppelganger has the following two key feature categories that we hope will improve population synthesis in practice:  
* __Bayesian Networks__. A [Bayesian network](https://en.wikipedia.org/wiki/Bayesian_network) is a directed graph of conditional probabilities for a set of random variables. Doppelganger allows users to easily build Bayesian nets from the [Public Use Microdata Sample (PUMS)](https://www.census.gov/programs-surveys/acs/technical-documentation/pums.html) data that is collected and distributed by the Census Bureau. Once created, these Bayesian nets can be traversed to create synthetic households and persons that have the same relationships, in the aggregate, as the source (in this case the PUMS) households and persons. Bayesian nets have the ability to both (a) add heterogeniety from synthetic populations drawn from a small sample of observations and (b) obscure the specific attributes of the observed sample.     
* __Convex Optimization__. Doppelganger, like most population synthesizer packages, allows users to allocate a set of observed or synthetic (created with Bayesian nets) households or persons to a geography such that the aggregate characteristics of the synthetic set matches the aggregate characteristics the user believes to be true about the geography. For example, it allows the user to allocate individual households to a [PUMA](https://www.census.gov/geo/reference/puma.html) such that the income distribution of the collection of households matches the income distribution from another data source (e.g., other summaries of the [American Community Survey](https://www.census.gov/programs-surveys/acs/) or [Decennial Census](https://www.census.gov/programs-surveys/decennial-census.html)). Doppelganger uses convex optimization to solve the allocation problem. Convex optimization has the attractive features of (a) generating a consistent solution, when one is available, and (b) allowing the user to introduce subjective weights to either prioritize one set of controls over another and/or efficiently overcome inconsistent controls.    

## What's Next?

Doppelganger version 0.1 is the beginning of our work -- a simple demonstration of the potential uses of the key features -- with population synthesizers, not the end. Up next: adding features and improving performance.

## Interested in Collaborating?

We'd love to hear from and collaborate with you. 
* If you're a government agency interested in deploying a population synthesizer, we'd be interested in understanding your needs and workflow to guide our next development push. 
* If you're an academic and/or model developer, we'd love to hear what enhancements would make your research or next deployment more successful. 
* If you're a developer, please share anything cool you're doing or would like to do with the toolkit. 

Please communicate with us via [GitHub's Issues](https://guides.github.com/features/issues/).  

## Credits

Doppelganger is inspired by:
* Judea Pearl's [*Probabilistic reasoning in intelligent systems: networks of plausible inference*](http://dl.acm.org/citation.cfm?id=52121);
* Vovsha, et. al.'s work on convex optimization described in [*New Features of Population Synthesis*](http://docs.trb.org/prp/15-5343.pdf); and,
* The open source ethos of [synthpop](https://github.com/UDST/synthpop).

## Licensing

Apache 2.0 © [Sidewalk Labs](sidewalklabs.com)
