# beep_guide
## 요약
이 파이썬 스크립트는 Tkinter와 Pygame 라이브러리를 활용하여 사용자 친화적인 인터페이스를 제공하고, 양치 데이터 수집 프로젝트를 위한 프레임워크를 구축합니다. 사용자에게 양치 지침을 제공하며, 오디오 신호와 시각적 안내를 통해 정확한 양치 위치를 지시합니다. 사용자가 지정된 양치 과정을 따를 때, 스크립트는 자동으로 양치 부위에 대한 레이블을 생성하고 이 데이터를 기록합니다. 양치 세션의 각 단계는 시간에 따라 관리되며, 세션 종료 시 사용자의 양치 패턴과 각 부위별 지속 시간을 포함한 데이터가 CSV 파일로 저장됩니다.

또한, 이 스크립트는 시리얼 통신을 지원하여, 양치 세션 중에 센서나 외부 장치로부터 실시간 데이터를 수집할 수 있도록 합니다. 이 기능은 물리적 움직임과 패턴을 데이터 수집 과정에 통합하여, 양치 기술의 분석을 향상시킵니다. 시리얼 통신 설정은 다양한 장치와 연결할 수 있도록 지정된 포트와 보드 레이트 설정을 통해 구성 가능하며, 스크립트는 어느 시점에 어떤 양치 부위를 대상으로 하는지에 따라 센서 데이터를 적절하게 레이블링하여 받을 수 있습니다. 이러한 종합적 접근 방식은 구강 건강 연구와 양치 기술 개선에 기여할 수 있는 상세한 분석을 위한 풍부한 데이터 세트를 보장합니다.

This Python script utilizes the Tkinter and Pygame libraries to offer a user-friendly interface and constructs a framework for a toothbrushing data collection project. It provides users with toothbrushing instructions, directing them to the precise brushing locations through audio signals and visual guidance. As users follow the specified brushing process, the script automatically generates labels for each brushing area and logs this data. Each phase of the brushing session is timed, and upon session completion, the data, including the user's brushing patterns and the duration spent on each area, is saved to a CSV file.

Moreover, the script supports serial communication, enabling the collection of real-time data from sensors or external devices during the toothbrushing session. This feature integrates physical movements and patterns into the data collection process, enhancing the analysis of brushing techniques. The serial communication setup can be configured to connect with various devices via specified port and baud rate settings, allowing the script to appropriately label and receive sensor data based on the targeted brushing area at any given moment. This comprehensive approach ensures a rich dataset for detailed analysis, contributing to oral health research and improvements in brushing technology.

## 화면구성
### 메인 화면
<img width="912" alt="main_screen" src="https://github.com/doyoon530/beep_guide/assets/150874253/3f338f56-3b34-48a8-8c0c-300c472d99c5">

### 구역 양치 화면
<img width="912" alt="areabrushing_screen_7s" src="https://github.com/doyoon530/beep_guide/assets/150874253/3a4c0dba-3cd7-4de3-9c03-ec4e6629ef0f">
<img width="912" alt="areabrushing_screen_2s" src="https://github.com/doyoon530/beep_guide/assets/150874253/4c8d44ca-29c4-4bd1-ba00-7e721c009f2b">
<img width="912" alt="areabrushing_screen_0s" src="https://github.com/doyoon530/beep_guide/assets/150874253/4d5c66f4-feac-4f8a-b7e3-8216d88e6f9f">

### 자유 양치 화면
<img width="912" alt="freebrushing_screen" src="https://github.com/doyoon530/beep_guide/assets/150874253/ac54b9f8-2de1-4239-afd5-bef9590c4e52">

## 레이블
<br>0. 대기 중 (Unknown)
<br>1. 앞니 바깥면 (IO)
<br>2. 왼쪽 바깥면 (LMO)
<br>3. 오른쪽 바깥면 (RMO)
<br>4. 왼쪽 아래 씹는면 (LUMC)
<br>5. 왼쪽 위 씹는면 (LWMC)
<br>6. 오른쪽 아래 씹는면 (RUMC)
<br>7. 오른쪽 위 씹는면 (RWMC)
<br>8. 앞니 위 안쪽면 (IUS)
<br>9. 앞니 아래 안쪽면 (IWS)
<br>10. 왼쪽 위 안쪽면 (LUMS)
<br>11. 왼쪽 아래 안쪽면 (LWMS)
<br>12. 오른쪽 위 안쪽면 (RUMS)
<br>13. 오른쪽 아래 안쪽면 (RWMS)
