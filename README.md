# bmecap-smartglasses
의료공학과 2025학년도 1학기 캡스톤디자인 - 스마트안경

# 제품 요약

본 프로젝트는 시각적 안내 및 물체 탐지 기능을 갖춘 스마트안경 개발을 목표로 합니다. 해당 시스템은 FastAPI 기반의 서버와 안드로이드 애플리케이션을 통해 사용자에게 실시간 서비스를 제공합니다. 안드로이드 애플리케이션은 블루투스 통신을 이용해 스마트안경과 연동됩니다.

# 제품 기능

1. 네비게이션 기능
   안경의 카메라 기반으로 단거리의 목적지까지의 경로를 실시간으로 안내합니다.   
   음성과 진동 등의 안내 기능을 추가하여 시각장애인이나 노인과 같은 사용자도 편리하게 사용할 수 있도록 설계됩니다.
   
2. 물건 찾기 기능
   특정 물건의 위치를 인식하고 사용자에게 안내하는 기능을 제공합니다.   
   스마트안경에 장착된 카메라와 컴퓨터 비전 기술을 이용하여 물체를 식별합니다.   
   `FastAPI` 서버에서 `OpenAI API` 통해 알고리즘을 운용합니다.

# 기술 스택

1. 서버 (Backend)
   - `FastAPI`: 경량 웹 프레임워크로 빠른 응답성과 비동기 처리를 통해 효율적인 데이터 통신을 수행합니다.
   - `Python`: 데이터 처리 및 머신러닝 모델 배포에 활용됩니다.
   - `OpenAI`: 자연어 처리 및 AI 기반 객체 탐지 기능을 강화하기 위해 활용됩니다.

2. 클라이언트 (Frontend)
   - `Android Studio`: 안드로이드 애플리케이션 개발 환경
   - `Java/Kotlin`: 안드로이드 앱 개발 언어
   - `Bluetooth API`: 스마트안경과의 블루투스 통신을 통해 실시간 데이터 전송 및 명령을 수행합니다.

# 시스템 구조

 - 사용자 ➔ 안드로이드 앱 ➔ FastAPI 서버 ➔ 스마트안경 (블루투스 통신)

# 데이터 흐름

 - 사용자가 스마트안경을 통해 명령을 입력합니다.
 - 안드로이드 애플리케이션이 해당 명령을 FastAPI 서버로 전송합니다.
 - FastAPI 서버는 명령을 처리하고, 필요한 경우 머신러닝 모델을 통해 객체 탐지 및 경로 탐색을 수행합니다.
 - 처리된 결과는 안드로이드 애플리케이션으로 전달되며, 이를 통해 사용자는 안내를 받습니다.
 - 안드로이드 애플리케이션은 블루투스 통신을 통해 스마트안경에 해당 정보를 전송합니다.

# 기대효과
1. 시각장애인 및 고령층과 같은 사용자들에게 보다 직관적이고 편리한 네비게이션 기능 제공
2. 물건 찾기 기능을 통해 일상생활에서의 편의성 향상
3. 의료공학과 특성에 맞는 헬스케어 및 복지 기술 연구 기회 제공
