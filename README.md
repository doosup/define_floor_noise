# TinyML을 이용한 층간소음 분석

## 1. 프로젝트 소개

### 1-1. 프로젝트 개요

인구밀도가 높은 한국의 주택 구조는 아파트와 빌라가 많다. 아파트는 빌라는 여러 가구가 모여 살기에 층간 소음이 있다. 층간 소음은 여전히 사회적으로 많은 문제를 일으키고 있다. 이 문제를 해결하기 위해 임베디드 기기에 TinyML을 적용하여 층간 소음을 모니터링하다가 층간 소음을 판단하는 지능형 기기를 만들고자 한다.

층간 소음 판단 기기는 위층에 있는 지능형 기기에 ZigBee 같은 무선 통신을 통해 소음 상태를 전달한다. 소음을 전달받은 위층의 지능형 기기는 거주자에게 소음 경고의 메시지를 전달하여, 소음을 자제하도록 한다.

사람들은 소음을 정량화 할수 없고, 감정적이므로 사람들이 나서서 층간 소음 문제를 해결하기는 어려운 문제다. 층간 소음을 판단하는 지능형 기기들이 소음을 정량화하고, 서로 통신하여, 사람들에게 소음 상태를 알려준다면 층간 소음으로 인한 이웃 간의 갈등의 문제는 많이 줄어들 것으로 예상된다.

<br>

### 1-2. 프로젝트 목표

이 프로젝트의 목표는 비용이 저렴한 MCU를 탑재한 임베디드 기기에 진동 센서를 내장하고, TinyML를 적용하여, 층간 소음을 판별하는 저렴한 지능형 기기를 만드는 것이다. 지능형 기기는 Zigbee를 이용하여, 서로 통신을 수행한다.

<br>

### 1-3. 프로젝트 주요 내용

층간 소음을 판별하고 소음 상태를 공유하는 지능형 기기를 개발은 다음과 같이 수행된다.

- 첫 번째는 층간 소음 데이터를 모은다.

- 두 번째는 모은 층간 소음 데이터를 CNN 모델을 통해서, 학습을 시킨다.

- 세 번째는 MCU와 진동 센서, Zigbee를 가진 임베디드 보드를 구성한다.

- 네 번째는 학습된 층간 소음을 판별하는 CNN 모델을 TinyML application에 포함시키고, 구성된 임베디드 보드에 베포한다.

- 다섯 번째 층간 소음을 판별하는 지능형 기기는 모니터링하다가 층간 소음이라고 판단되면, 위층의 지능형 기기에 무선 통신을 수행한다. 위층의 지능형 기기는 층간 소음 메시지를 받은 후 층간 소음 알람을 알린다.

<br>

## 2. 파일 구성 및 활동 내용

주 활동 내용은 다음과 같으며, 각 활동에 대한 자세한 내용은 각가의 폴더에 있는 README.md 파일을 참고한다.

1. 선행 연구 조사 및 센서 조사

2. 데이터 처리 프로세스 설계

3. CNN 모델 및 TF Lite 변환 스터디

4. 샘플 데이터 수집

5. 샘플 데이터 분석 및 CNN 모델 생성

6. 실제 데이터 수집

7. 실제 데이터 분석 및 CNN 모델 생성

8. 임베디드 보드 구성

9. 통합 테스트
# define_floor_noise
