FROM rocker/binder
LABEL maintainer='James Howison'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/howisonlab/holepunch_test/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-04-15/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
