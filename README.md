# Validator

## Install Dependencies

    sudo apt update
    sudo apt install curl git make jq build-essential gcc unzip wget lz4 aria2 pv -y
    

## Install Go Language

    cd $HOME && \
    ver="1.22.0" && \
    wget "https://golang.org/dl/go$ver.linux-amd64.tar.gz" && \
    sudo rm -rf /usr/local/go && \
    sudo tar -C /usr/local -xzf "go$ver.linux-amd64.tar.gz" && \
    rm "go$ver.linux-amd64.tar.gz" && \
    echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> ~/.bash_profile && \
    source ~/.bash_profile && \
    go version

## Install Story Geth

    wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/geth-public/geth-linux-amd64-0.9.2-ea9f0d2.tar.gz
    tar -xvf geth-linux-amd64-0.9.2-ea9f0d2.tar.gz
    cp geth-linux-amd64-0.9.2-ea9f0d2.tar.gz/geth /usr/local/bin/


## Install Story

    wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/story-public/story-linux-amd64-0.9.11-2a25df1.tar.gz
    tar -xvf story-linux-amd64-0.9.11-2a25df1.tar.gz
    cp story-linux-amd64-0.9.11-2a25df1.tar.gz/story /usr/local/bin/


## Init Geth

    screen -S Geth
    geth --iliad --syncmode full
Detach the session by Ctrl+A+D


## Install Go Language

    screen -S Story
    story init  --network iliad --moniker {NAME}
Install Go Language

    story run





