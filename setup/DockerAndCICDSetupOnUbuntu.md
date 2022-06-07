# DOCKER 설치
https://dongle94.github.io/docker/docker-ubuntu-install/#gpg-%ED%82%A4-%EB%B0%8F-%EC%A0%80%EC%9E%A5%EC%86%8C-%EC%B6%94%EA%B0%80

## HTTP 패키지 설치
```
$ sudo apt update
$ sudo apt-get install -y ca-certificates \ 
    curl \
    software-properties-common \
    apt-transport-https \
    gnupg \
    lsb-release
```

## GPG 키 및 저장소 추가
```
$  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```


## Docker CE 설치
```
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
```

# Dcoker 권한처리
## 내가 포함된 권한 확인(ubuntu가 계정이름일 때)
```
$ sudo groups $USER
> root
```

## docker라는 그룹명 추가(보통 이미 추가 되어 있음)
```
$ sudo groupadd docker
```

## 그룹 추가
```
sudo usermod -aG docker $USER
```

# CICD 설정 (Git 설정, JAVA, MVN)
## Git clone 하기
```
$ git clone -b {branch명} {git url} {생성폴더이름:생략시 프로젝트명}
```

## git 계정등록(cache는 기간제한)
```
$ git config credential.helper store
$ git pull
> id, pw 입력
```

## JDK설치, MVN 설치
```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install openjdk-11-jdk
$ sudo apt install maven
```
