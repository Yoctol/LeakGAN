FROM tensorflow/tensorflow:1.2.1-devel-gpu 
COPY Pipfile Pipfile.lock ./
RUN apt-get update && apt-get install -y --no-install-recommends \
	&& pip install --upgrade pip==19.1.1 \
	&& pip install pipenv==v2018.11.26 \
	&& pipenv install --deploy --system \
  && rm -rf /var/lib/apt/lists/*
COPY . .
