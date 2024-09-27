Submitting a paper to JOSE
==========================

Preparing your JOSE submission should be a simple task, once you have a complete
software or learning module you wish to publish.

## The two submission types

JOSE accepts two types of submissions: (1) computational learning modules, created as open educational resources (OER), and (2) open-source software, created as educational technology or infrastructure.

## Submission requirements

JOSE submissions must be fully open, under the [Open Definition](http://opendefinition.org/).
This means that any text content or graphical objects should be under a
Creative Commons license (ideally [CC-BY](https://creativecommons.org/licenses/by/4.0/))
and code components should be under an [OSI-approved license](https://opensource.org/licenses).

Computational learning modules should be complete and immediately usable for
self-learning or adoption by other instructors. They should make a clear
contribution to teaching and learning of any subject, supported by computing.
JOSE is not focused in OER for "learning to code" as much as "coding to learn."

Software submissions should make a clear contribution to the available open-source software that supports teaching and learning, or makes an educational process better (e.g., faster, easier, simpler). Examples include software to auto-grade student work, learning management systems, and student collaboration frameworks. Software should be feature-complete (no half-baked solutions).

## What about novelty?

Authors make the case for their submission's contribution in the paper, under the
heading "Statement of Need." The criterion is less one of novelty, than need:
submissions targeting subjects or applications already addressed by other resources
are eligible, if the authors make a case for why they might be adopted by learners
or other instructors. For example, authors could say that they approach a topic
differently, that they update material to modern contexts, that the need is born of
a new educational program, or a conference tutorial or other informal-learning scenario.

## How to prepare a software submission?

Before starting your submission, you should:

- Have the software available in an open repository (GitHub, Bitbucket, etc.) under an [OSI-approved license](https://opensource.org/licenses).
- Write a short Markdown file titled `paper.md` with title, author names and affiliations, containing a description of the software, statement of need, and key references.
- References should be included in a BibTeX file called `paper.bib`

Once you have those items in place, [submit](https://jose.theoj.org/papers/new) via the JOSE web app.

## How to prepare a learning-module submission?

Before starting your submission, you should:

- Have the content in an open repository, under a Creative Commons license (ideally CC-BY), and any code components under an [OSI-approved license](https://opensource.org/licenses).
- Write a short Markdown file titled `paper.md` with title, author names and affiliations, containing a description of the module, a summary of its contents, a statement of need, and key references.
- References should be included in a BibTeX file called `paper.bib`

Once you have those items in place, [submit](https://jose.theoj.org/papers/new) via the JOSE web app.

## What should my paper contain?

JOSE papers should:

- List all authors and affiliations.
- Describe the submission, and explain its eligibility for JOSE.
- Include a "Statement of Need" section, explaining how the submitted artifacts contribute to computationally enabled teaching and learning, and describing how they might be adopted by others.
- For software submissions, describe the functionality of the software, usage and recent experience of use in teaching and learning situations.
- For learning modules, describe the learning objectives, content, instructional design, and experience of use in teaching and learning situations.
- Tell us the "story" of the project: how did it come to be?
- Cite key references, including a link to the open archive of the sofware or the learning module.

JOSE welcomes submissions with diverse educational contexts. You should write your
paper for a non-specialist reader. Your submission should probably be around 1000
words (or around two pages).

The goal is that someone reading the JOSE paper has enough information to decide
if they'd be interested in adoping the learning module or software. Readers will
want to know how the content/software has been used, and how they would adopt it.
They may also want to be persuaded that the authors have put careful work on
creating the material, and have experience teaching with it.

JOSE papers contain a limited set of metadata, plus Summary & Reference sections.
We explicitly do not publish long-form articles, because the scholarship represented
by a JOSE article is contained in the software or learning modules themselves.
Expected length is around 1000 words max.

## Example paper and bibliography

This example `paper.md` is adapted from the JOSS paper _Gala: A Python package for galactic dynamics_ by Adrian M. Price-Whelan [http://doi.org/10.21105/joss.00388](http://doi.org/10.21105/joss.00388):

```
---
title: 'Gala: A Python package for galactic dynamics'
tags:
  - Python
  - astronomy
  - dynamics
  - galactic dynamics
  - milky way
authors:
  - name: Adrian M. Price-Whelan
    orcid: 0000-0003-0872-7098
    affiliation: "1, 2" # (Multiple affiliations must be quoted)
  - name: Author Without ORCID
    affiliation: 2
affiliations:
 - name: Lyman Spitzer, Jr. Fellow, Princeton University
   index: 1
 - name: Institution 2
   index: 2
date: 13 August 2017
bibliography: paper.bib

# Optional fields if submitting to a AAS journal too, see this blog post:
# https://blog.joss.theoj.org/2018/12/a-new-collaboration-with-aas-publishing
aas-doi: 10.3847/xxxxx <- update this with the DOI from AAS once you know it.
aas-journal: Astrophysical Journal <- The name of the AAS journal.
---

# Summary

The forces on stars, galaxies, and dark matter under external gravitational
fields lead to the dynamical evolution of structures in the universe. The orbits
of these bodies are therefore key to understanding the formation, history, and
future state of galaxies. The field of "galactic dynamics," which aims to model
the gravitating components of galaxies to study their structure and evolution,
is now well-established, commonly taught, and frequently used in astronomy.
Aside from toy problems and demonstrations, the majority of problems require
efficient numerical tools, many of which require the same base code (e.g., for
performing numerical orbit integration).

``Gala`` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for ``Gala`` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. ``Gala`` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the ``Astropy`` package [@astropy] (``astropy.units`` and
``astropy.coordinates``).

``Gala`` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in ``Gala`` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike.

# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$

Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$


# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this: ![Example figure.](figure.png)

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
```

Example `paper.bib` file:

```
@article{Pearson:2017,
  	Adsnote = {Provided by the SAO/NASA Astrophysics Data System},
  	Adsurl = {http://adsabs.harvard.edu/abs/2017arXiv170304627P},
  	Archiveprefix = {arXiv},
  	Author = {{Pearson}, S. and {Price-Whelan}, A.~M. and {Johnston}, K.~V.},
  	Eprint = {1703.04627},
  	Journal = {ArXiv e-prints},
  	Keywords = {Astrophysics - Astrophysics of Galaxies},
  	Month = mar,
  	Title = {{Gaps in Globular Cluster Streams: Pal 5 and the Galactic Bar}},
  	Year = 2017
}

@book{Binney:2008,
  	Adsnote = {Provided by the SAO/NASA Astrophysics Data System},
  	Adsurl = {http://adsabs.harvard.edu/abs/2008gady.book.....B},
  	Author = {{Binney}, J. and {Tremaine}, S.},
  	Booktitle = {Galactic Dynamics: Second Edition, by James Binney and Scott Tremaine.~ISBN 978-0-691-13026-2 (HB).~Published by Princeton University Press, Princeton, NJ USA, 2008.},
  	Publisher = {Princeton University Press},
  	Title = {{Galactic Dynamics: Second Edition}},
  	Year = 2008
}

@article{gaia,
    author = {{Gaia Collaboration}},
    title = "{The Gaia mission}",
    journal = {\aap},
    archivePrefix = "arXiv",
    eprint = {1609.04153},
    primaryClass = "astro-ph.IM",
    keywords = {space vehicles: instruments, Galaxy: structure, astrometry, parallaxes, proper motions, telescopes},
    year = 2016,
    month = nov,
    volume = 595,
    doi = {10.1051/0004-6361/201629272},
    adsurl = {http://adsabs.harvard.edu/abs/2016A%26A...595A...1G},
}

@article{astropy,
    author = {{Astropy Collaboration}},
    title = "{Astropy: A community Python package for astronomy}",
    journal = {\aap},
    archivePrefix = "arXiv",
    eprint = {1307.6212},
    primaryClass = "astro-ph.IM",
    keywords = {methods: data analysis, methods: miscellaneous, virtual observatory tools},
    year = 2013,
    month = oct,
    volume = 558,
    doi = {10.1051/0004-6361/201322068},
    adsurl = {http://adsabs.harvard.edu/abs/2013A%26A...558A..33A}
}
```

Note that the paper ends with a References heading, and the references are built
automatically from the content in the `.bib` file. You should enter in-text
citations in the paper body following correct [Markdown citation syntax](https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html#citation_syntax).

## Submitting your paper

Submission is as simple as:

- Filling in the [short submission form](http://jose.theoj.org/papers/new)
- Waiting for the managing editor to start a pre-review issue over in the JOSS reviews repository: https://github.com/openjournals/jose-reviews

## No submission fees

There are no fees for submitting or publishing in JOSE. You can read more about our [cost and sustainability model](http://joss.theoj.org/about#costs).

## Preprint Policy

Authors are welcome to submit their papers to a preprint server ([arXiv](https://arxiv.org/), [bioRxiv](https://www.biorxiv.org/), [SocArXiv](https://socopen.org/), [PsyArXiv](https://psyarxiv.com/) etc.) at any point during the submission and review process.

Submission to a preprint server is _not_ considered a previous publication.

## Authorship

Purely financial (such as being named on an award) and organizational (such as general supervision of a research group) contributions are not considered sufficient for co-authorship of JOSE submissions, but active project direction and other forms of non-code contributions are. The authors themselves assume responsibility for deciding who should be credited with co-authorship, and co-authors must always agree to be listed. In addition, co-authors agree to be accountable for all aspects of the work, and to notify JOSE if any retraction or correction of mistakes are needed after publication.

## Submissions using proprietary languages/dev environments

We strongly prefer software that doesn't rely upon proprietary (paid for) development environments/programming languages. However, provided _your submission meets our requirements_ (including having a valid open source license) then we will consider your submission for review. Should your submission be accepted for review, we may ask you, the submitting author, to help us find reviewers who already have the required development environment installed.

## The review process

We encourage you to familiarize yourself with our [review criteria](review_criteria.html) as this will help you understand what our reviewers will be looking for. Broadly speaking though, provided you have followed our pre-submission steps and meet our submission requirements then you should expect a rapid review (typically less than two weeks).

After submission:

- The Editor-in-Chief will carry out an initial check of your submission, and proceed to assign a handling editor.
- The handling editor will assign two or more JOSE reviewers, and the review will be carried out in the [JOSE reviews repository](https://github.com/openjournals/jose-reviews).
- Authors will respond to reviewer-raised issues (if any are raised) on the submission repository's issue tracker. Reviewer and editor contributions, like any other contributions, should be acknowledged in the repository.
- Upon successful completion of the review, deposit a copy of your (updated) repository with a data-archiving service such as [Zenodo](https://zenodo.org/) or [figshare](https://figshare.com/), get a DOI for the archive, and update the review issue thread with the DOI.
- After we assign a DOI for your accepted JOSE paper, its metadata is deposited with CrossRef and listed on the JOSE website.
- The review issue will be closed, and an automatic tweet from [@JOSE_TheOJ](https://twitter.com/JOSE_TheOJ) will announce it!

If you want to learn more details about the review process, take a look at the [reviewer guidelines](reviewer_guidelines.html).
