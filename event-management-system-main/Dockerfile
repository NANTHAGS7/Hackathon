FROM python:alpine

WORKDIR /app

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV public_key=pk_test_51N2BrwSEKG4vuy5hIvfmAfjapR0KOwTtxr4qeCJxKfXTlEV1WsLVtfvoIlPsRpkgDRui2SxUt4mV26tXN04LINVX00MKOd8pVk

RUN apk add --no-cache gcc musl-dev linux-headers

COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt
RUN pip install plotly


EXPOSE 5000

COPY . .

CMD ["flask", "run"] 