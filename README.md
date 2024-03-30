<h1 align='center'>Install mamba_ssm & causal_conv1d</h1>

# Two approaches (Docker Installation & Conda Installation)
### ___Strongly recommend to create a new conda-environment!!!___

## Approach 1: Docker

### <1> If you have not installed docker, run these commands step by step:

```shell
1. yum install -y yum-utils device-mapper-persistent-data lvm2

2. yum-config-manager --add-repo https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo

3. yum install -y docker-ce

4. systemctl start docker

5. systemctl enable docker

6. docker pull kom4cr0/cuda11.7-pytorch1.13-mamba1.1.1:1.1.1
```

### <2>If you have installed docker, just run the 6th command:

```shell
docker pull kom4cr0/cuda11.7-pytorch1.13-mamba1.1.1:1.1.1
```



## Approach 2: Conda environment

```shell
1. conda create -n mamba python=3.10

2. conda activate mamba

3. conda install cudatoolkit==11.7 -c nvidia

4. pip install torch==1.13 torchvision==0.14.0 torchaudio==0.13.0 --index-url https://download.pytorch.org/whl/cu117

5. conda install -c "nvidia/label/cuda-11.7.0" cuda-nvcc

6. conda install packaging

7. pip install causal-conv1d==1.1.1

8. pip install mamba-ssm
```
