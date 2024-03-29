# 2023 DY CG Pwn Docker Image

위 이미지는 2023 덕영고 Cyber Guardians 포너블 수업에 사용할 docker 이미지입니다.
이 repo와 package는 MIT LICENSE가 적용 됩니다.

## docker 컨테이너 생성

### ubuntu 22.04

```bash
docker run -d -p 2204:22 --name new_pwn_22.04 ghcr.io/zeroday2162/2023-cg-pwn:22.04
```

### ubuntu 20.04

```bash
docker run -d -p 2004:22 --name new_pwn_20.04 ghcr.io/zeroday2162/2023-cg-pwn:20.04
```

ubuntu 22.04는 2204, ubuntu 20.04는 2004 포트를 이용해 ssh로 서버에 접근이 가능하며, root와 user01 ~ 10의 유저가 설정되어 있습니다.

GDB-peda, python3 pwntools, One-shot gadget 같은 포너블에 필요한 기본 패키지 또한 설정 되어 있고, 일반 유저와 root 유저가 모든 환경을 사용할 수 있습니다.

## ssh 접속

```bash
ssh -p 2204 USERNAME@SERVER_IP # ubuntu 22.04
ssh -p 2004 USERNAME@SERVER_IP # ubuntu 22.04
```

### Default ID, Password

- ROOT
	- ID: root
	- PW: zerocoke
- USER
	- ID: user01 ~ 10
	- PW: abc1234#
