
======================
    did
======================


LICENSE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Copyright Red Hat

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

GOAL
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Python 문법을 익히고 사용된 라이브러리의 공식문서를 찾아보면서 오픈소스를 분석하고 제작자의 의도를 파악하는 능력을 기르기 위해 해당 프로젝트를 선택.

Requirements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
pypi package == 0.22.1

python >= 3.9  

How to install & Run
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Dockerfile을 만들 디렉토리 만들기
2. vi 에디터를 통해 Dockerfile을 만들고 Dockerfile에 들어갈 내용 작성하기
3. docker build -t <이미지 이름:버전> . -> 명령어를 통해 이미지 생성
4. docker run -dit <이미지 이름:버전> -> 명령어로 컨테이너 생성
5. docker exec -it <컨테이너 이름 또는 ID> /bin/bash -> 컨테이너 접속
6. did --help 명령어 실행 -> did <option> 확인 가능
7. exit 명령어로 컨테이너 밖으로 빠져나오기
8. docker ps -> 실행중인 컨테이너 확인
9. docker stop <컨테이너 이름 또는 ID> -> 컨테이너 실행중이라면 종료


디렉토리 구조
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
did/
├── bin/
│   └── did                 # CLI 실행 스크립트
├── config/                 # 예제 설정 파일들
├── data/                   # 테스트용 샘플 데이터
├── doc/                    # 문서화 (reStructuredText 형식)
├── examples/               # 예제 사용법 스크립트
├── src/
│   └── did/
│       ├── cli.py          # CLI 진입점
│       ├── config.py       # 설정 로딩 로직
│       ├── plugins/        # 다양한 plugin 모듈 (github, nitrate 등)
│       │   ├── __init__.py
│       │   ├── github.py
│       │   └── nitrate.py
│       ├── stats.py        # 통계 수집 및 출력 모듈
│       └── __init__.py
├── tests/
│   └── test_cli.py         # 테스트 코드들
├── LICENSE
├── README.md
├── requirements.txt
└── setup.py                # 설치 설정 파일
