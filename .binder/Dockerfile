FROM rocker/binder:4.0.2
LABEL maintainer='Daniel Nothaft'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/danote/Oman-packers-2018-2019/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2021-07-22/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
