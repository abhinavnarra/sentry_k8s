# Sentry_k8s

## Setup  Environment

### Install system dependencies
    sudo pip install terraform

### Clone the code

    cd ~/
    git clone git@github.com:abhinavnarra/sentry_k8s.git

### Create virtual environment and activate

    virtualenv -p python3 ~/env/sentry
    source ~/env/sentry/bin/activate

## setup eks cluster

    cd sentry_k8s/terraform/eks
    terraform init
    terraform plan 
    terraform apply --autoapprove

## Execute sentry

    kubectl apply -f sentry.yml