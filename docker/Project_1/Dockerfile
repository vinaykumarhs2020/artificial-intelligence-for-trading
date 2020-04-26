FROM jupyter/minimal-notebook:7c45ec67c8e7

COPY requirements.txt /tmp/requirements.txt
RUN /opt/conda/bin/python -m pip install cython
RUN /opt/conda/bin/python -m pip install -r /tmp/requirements.txt

# CVXPY fails to build normally. Hence need to update numpy version
RUN /opt/conda/bin/python -m pip uninstall -y cvxpy
RUN /opt/conda/bin/python -m pip install numpy==1.16
RUN /opt/conda/bin/python -m pip install cvxpy==1.0.3

