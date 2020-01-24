################## BASE IMAGE ######################
FROM continuumio/miniconda3:4.7.12

ENTRYPOINT []
WORKDIR /opt/conda/bin

RUN conda install --yes -c bioconda bedtools
RUN conda install --yes -c bioconda -c conda-forge cnv_facets=0.15.0


RUN apt-get update && apt-get install -y \
  curl \
  less \
  tree \
  vim \
  wget \
  procps \
  && rm -rf /var/lib/apt/lists/*

ENV PATH /opt/conda/envs/ngs-pipeline/bin:/opt/conda/bin:$PATH
