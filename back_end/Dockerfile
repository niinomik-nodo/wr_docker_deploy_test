FROM python:3.9-buster
ENV PYTHONUNBUFFERED=1

WORKDIR /usr/src/app
COPY api ./

RUN pip3 install --upgrade pip
RUN pip3 install fastapi
RUN pip3 install "uvicorn[standard]"
RUN pip3 install requests

ENTRYPOINT ["uvicorn", "back_end.api.main:app", "--host", "0.0.0.0", "--reload"]
