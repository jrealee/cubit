# syntax=docker/dockerfile:1
FROM opentensorfdn/bittensor:4.0.1

# Install cubit
COPY . /cubit/
RUN cd /cubit && \
    python3 -m pip install -r requirements.dev.txt && \
    python3 setup.py build_ext --inplace

ENV PYTHONPATH "${PYTHONPATH}:/cubit"
