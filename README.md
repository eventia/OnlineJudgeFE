# 온라인저지 Online Judge 프론트 엔드 (VER 0.2a)

## 개발자

+ 바람(2019.08.29.)

## 특징

+ 중국 QingDao University 오픈소스 
+ github/ndb796/OnlineJudgeFE 프론트소스 
+ 웹팩3(Webkpack3)를 활용한 다중 페이지
+ 쉽게 사용할 수 있는 코드 에디터
+ E-Charts를 활용한 시각화 모듈
+ 사용자 친화적인 명령어 기능

## 설치 방법

노드 JS **v6.11** 버전이 설치가 되어 있어야 합니다.

```
# GCP 의 VM 사용
g1-small 혹은 g1-standard-1 사용 (g1-standard-1 추천, 1 CPU, 3.75G )
Ubuntu 16.04 LTS , 10G 사용
http 트랙픽 허용 사용

 
# nodejs 와 npm 설치
sudo apt-get update && sudo apt-get install -y vim python-pip curl git
sudo apt update & sudo apt upgrade -y
sudo apt install nodejs-legacy
sudo apt install npm

# n 설치
sudo npm clean cache -f
sudo npm install -g n
sudo n 6.11

# github 에서 FE 다운
mkdir OnlineJudge
cd OnlineJudge
git clone https://github.com/QingdaoU/OnlineJudgeFE.git 
cd OnlineJudgeFE

# 소스 수정
cd src/pages/oj
nano App.vue
src 디렉토리내부에 있는 파일들을 살피고 필요한 부분을 알아서 수정한다.

# 편집 후 ~/OnlineJudge/OnlineJudgeFE 디렉토리로 이동하여 빌드
cd ../../..
sudo npm install

# FroneEnd 를 채점서버와 연결(연동)
NODE_ENV=development sudo npm run build:dll 
export TARGET=http://[채점서버ip주소]/
	http://35.225.173.64/
npm run dev

```

실행 이후의 Host의 80번 포트 혹은 443번 포트와 본 서버의 8080 포트와 포트 포워딩을 해주어야 합니다.


## 데모

http://luco.cf

## 브라우저 지원

+ 인터넷 익스플로러 10 이상
+ 가능한 chrome 사용을 권장함

## 온라인 저지 백 엔드에 대해서

+ 기본적으로 온라인 저지 백 엔드는 Qingdao University의 Online Judge Server 모듈의 Docker Version을 사용합니다.
+ 현재 기존의 레거시 코드 한글 패치를 적용한 상황입니다.

## 향후 개발 방향

+ 향후 본 서버에서 추출된 사용자 채점 정보를 이용해 학생들의 수준을 판별하고 분류합니다.
+ REST API를 활용한 Micro Service 원칙을 철저하게 따릅니다.
+ 정보올림피아드 준비를 하는 초,중,고등학생들을 위한 문제은행과 강의 컨텐츠를 지속적으로 추가합니다.

## 오픈소스 라이센스

[MIT](http://opensource.org/licenses/MIT)
