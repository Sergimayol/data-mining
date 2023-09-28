FROM rocker/r-ver:latest

WORKDIR /home/rstudio

RUN apt-get update && apt-get install -y \
    build-essential \
    software-properties-common \
    git \
    pandoc

RUN R -e 'install.packages(c("devtools", "languageserver"))' && \
    R -e 'devtools::install_github("REditorSupport/languageserver")' && \
    R -e 'install.packages(c("ggplot2", "GGally"))'
# && \ R -e 'install.packages("httpgd")'
