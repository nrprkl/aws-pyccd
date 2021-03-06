# About

Project for running Open Data Cube on AWS.


## Setup

This project requires miniconda: https://conda.io/docs/install/quick.html

```
conda config --add channels conda-forge

conda create --name aws-pyccd python=3.5 datacube

source activate aws-pyccd

pip install lcmap-pyccd

conda install jupyter matplotlib scipy -y
```

## Credentials

This project uses Boto3 to work with AWS, you will need to add credentials
to `~/.aws/config` that allow you to write to an S3 bucket.

```
[default]
aws_access_key_id = YOUR_ACCESS_KEY
aws_secret_access_key = YOUR_SECRET_KEY
```

## Credentials

This project uses Boto3 to work with AWS, you will need to add credentials
to `~/.aws/config` that allow you to write to an S3 bucket.

```
[default]
aws_access_key_id = YOUR_ACCESS_KEY
aws_secret_access_key = YOUR_SECRET_KEY
```

## Usage

Start the notebook server.

```
bin/notebook-server
```

If AWS RDS is not available, a local Docker instance of Postgres can be easily run:

```docker run --name some-postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword postgres```

## License

TBD
