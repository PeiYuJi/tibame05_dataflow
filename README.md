# dataflow

# 環境設定

#### 安裝 pipenv

    pip install pipenv==2022.4.8

#### set pipenv

    pipenv --python ~/.pyenv/versions/3.8.10/bin/python

#### 安裝 repo 套件

    pipenv sync

#### 建立環境變數

    ENV=DEV python genenv.py
    ENV=DOCKER python genenv.py
    ENV=PRODUCTION python genenv.py

#### 排版

    black -l 80 src/

# Docker

#### build docker image

    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.1 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.1.arm64 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.2 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.2.arm64 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.3 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.3.arm64 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.4 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.4.arm64 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.5 .
    docker build -f with.env.Dockerfile -t linsamtw/tibame_dataflow:0.0.5.arm64 .

#### push docker image

    docker push linsamtw/tibame_dataflow:0.0.1
    docker push linsamtw/tibame_dataflow:0.0.1.arm64
    docker push linsamtw/tibame_dataflow:0.0.2
    docker push linsamtw/tibame_dataflow:0.0.2.arm64
    docker push linsamtw/tibame_dataflow:0.0.3
    docker push linsamtw/tibame_dataflow:0.0.3.arm64
    docker push linsamtw/tibame_dataflow:0.0.4
    docker push linsamtw/tibame_dataflow:0.0.4.arm64
    docker push linsamtw/tibame_dataflow:0.0.5
    docker push linsamtw/tibame_dataflow:0.0.5.arm64

#### pull docker image

    docker pull linsamtw/tibame_dataflow:0.0.1
    docker pull linsamtw/tibame_dataflow:0.0.2

## deploy-airflow:
	DOCKER_IMAGE_VERSION=0.0.1 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.1.arm64 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.2 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.2.arm64 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.3 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.3.arm64 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.4 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.4.arm64 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.5 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
	DOCKER_IMAGE_VERSION=0.0.5.arm64 docker stack deploy --with-registry-auth -c docker-compose-airflow.yml airflow
