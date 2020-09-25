FROM python:3.8 AS build
RUN pip install --no-cache-dir dask distributed bokeh

FROM python:3.8-slim
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/lib/python3.8/site-packages /usr/local/lib/python3.8/site-packages
