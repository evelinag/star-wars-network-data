# Star Wars social networks
[![DOI](https://zenodo.org/badge/147848071.svg)](https://zenodo.org/badge/latestdoi/147848071)

This repository contains the social network of Star Wars characters extracted from movie scripts. In short, two characters are connected if they speak together within the same scene. The data contain characters and links from episodes I to VII.

How the data were created is described in my blog posts:
- [The Star Wars social network](http://evelinag.com/blog/2015/12-15-star-wars-social-network/index.html)
- [Star Wars social network: Force Awakens](http://evelinag.com/blog/2016/01-25-social-network-force-awakens/index.html)

The associated code is available in the main repository [evelinag/StarWars-social-network](https://github.com/evelinag/StarWars-social-network).

Contents of the files are the following:

* `starwars-episode-N-interactions.json` contains the social network extracted from Episode N, where the links between characters are
defined by the times the characters speak within the same scene.

* `starwars-episode-N-mentions.json` contains the social network extracted from Episode N, where the links between characters are
defined by the times the characters are mentioned within the same scene.

* `starwars-episode-N-interactions-allCharacters.json` is the `interactions` network with R2-D2 and Chewbacca added in using 
data from `mentions` network.

* `starwars-full-...` contain the corresponding social networks for the whole set of 6 episodes.

## Description of networks
The json files representing the networks contain the following information:

### Nodes
The nodes contain the following fields:
- name: Name of the character
- value: Number of scenes the character appeared in
- colour: Colour in the visualization

### Links
Links represent connections between characters. The link information corresponds to: 
- source: zero-based index of the character that is one end of the link, the order of nodes is the order in which they are listed in the “nodes” element
- target: zero-based index of the character that is the the other end of the link. 
- value: Number of scenes where the “source character” and “target character” of the link appeared together.
Please not that the network is *undirected*. Which character represents the source and the target is arbitrary, they correspond only to two ends of the link.

## Citing the dataset

If you use the dataset in your work, please use the following citation:

Gabasova, E. (2016). Star Wars social network. DOI: https://doi.org/10.5281/zenodo.1411479.

    @misc{gabasova_star_wars_2016,
      author  = {Evelina Gabasova},
      title   = {{Star Wars social network}},
      year    = 2016,
      url     = {https://doi.org/10.5281/zenodo.1411479},
      doi     = {10.5281/zenodo.1411479}
     }
