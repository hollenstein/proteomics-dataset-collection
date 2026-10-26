## Title

Building a Community Dataset Collection for Proteomics

## Abstract

Proteomics software development often requires small, representative datasets for development, testing, compatibility checks, usage examples, and education. Finding suitable data can be difficult, as public datasets are often very large and may be difficult to discover or acquire for a specific use case.

This project aims to build a community-maintained collection of reusable proteomics datasets, together with simple infrastructure to describe, version, publish, and acquire them. Datasets will be described by lightweight manifests, while the actual files can remain hosted by existing public repositories.

During the hackathon, we will define the minimal manifest specification, establish the collection and its maintenance workflow, curate initial datasets, and develop a simple Python consumer that can retrieve complete datasets or individual files. The aim is to create a community resource that can continue to grow and support proteomics software projects.

**Examples and possible use cases**

The collection should support different kinds of reusable datasets, for example:

- **Tiny raw files** small enough for CI pipelines, covering different vendors, instruments, and acquisition strategies, for software that directly consumes raw data. Potential users include projects such as mzPeak and timsCompare.
- **Software output collections** such as search-engine results or outputs from different software versions, for testing compatibility and importers.
- **Example and educational datasets** containing representative biological data for tutorials, documentation, demonstrations, or GUIs.
- **Curated datasets from existing projects**, where a manifest bundles the files needed for a particular use case. This could also include resources such as Proteobench datasets.

The initial collections and their priorities will be defined during the hackathon.

## Project Plan

**Goals for the Hackathon**

The main goals are to:

- Define a minimal **dataset manifest specification**.
- Design a **GitHub-based workflow** for creating, validating, and maintaining manifests.
- Build an initial small curated **dataset manifest collection**.
- Publish an **initial release** of the public reference collection.
- Develop a **simple consumer and CLI** that can download a complete dataset or an individual file and validate the downloaded files.

Participants are encouraged to bring datasets or dataset requirements from their own projects.

**Follow-up**

After the hackathon, we will:

- Continue developing the Python consumer into a robust, easy-to-use tool.
- Develop additional language implementations where there is community interest, including an R client.
- Continue producing tiny raw data for software CI purposes, growing the initial collection beyond the datasets curated during the event.

The code, manifests, and collection infrastructure will be released under permissive open-source licenses.

## Technical Details

- GitHub and GitHub Actions will be used for development and validation of the dataset collection, with **Zenodo** for permanent versioned releases.
- The reference consumer will initially be implemented in **Python**. Pooch could be used as an initial download layer, and Cyclopts is one option for the CLI.
- The manifest/interface should be language-independent, so alternative implementations are welcome.

**Datasets and availability**

We will start the hackathon with a small collection of tiny raw files brought from our facility, together with a suitable example dataset from ProteoBench.

Additional public datasets can be selected and curated by participants, while the hackathon can also define requirements for future datasets to be contributed by our facility or other collaborators.