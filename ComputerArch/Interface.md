# 인터페이스
서로 다른 두 장치에서 상호 통신이 가능하도록 조화시키는 역할

## I/O 버스와 인터페이스 장치
- CPU가 주소 버스에 통신할 인터페이스 주소 전송
- 해당 인터페이스가 데이터 버스와 장치 사이 연결

## CPU <-> 주기억 장치 및 I/O 장치 통신 방식
- 메모리 맵 입출력 (Memory-Mapped I/O)
    - 메모리 주소 일부를 I/O 장치에 할당
    - 메모리 자료를 R/W 하는 것처럼 I/O 장치와 송수신
    - 메모리와 I/O 장치 명렁 구분 없이 사용
    - I/O 장치가 차지하는 부분의 주소를 메모리로 사용 불가
- 포트 맵 입출력 (Port-Mapped I/O)
    - I/O 장치에 메모리와 별도의 주소 공간 할당
    - 전용 I/O 명령 사용
    - 주소 영역 전체를 메모리로 쓸 수 있다.
    - 명령이 구분되어 프로그램 분석 향상
    - 별도의 명령, 제어가 필요해 내부 구조 복잡

## 인터페이스 기능
- 속도차 극복
    - 버퍼에 R/W 후 CPU에 알림
- 데이터 형식 변환
    - CPU 워드/더블워드 <-> I/O 장치 바이트
- 오류 검사

## 인터페이스 종류
- PS/2 포트
    - 키보드, 마우스
    - 6핀
    - IBM 개발
- 직렬 포트 (Serial Port)
    - 1비트씩 전송
- 병렬 포트 (Parallel Port)
    - 1바이트씩 전송
    - 주로 프린터 사용
- USB (Universal Serial Bus)
    - 자체 버스, 컨트롤러를 쓰는 직렬 포트
    - 주변 기기를 PnP로 인식
    - 확장 연결로 Daisy Chain 연결 가능
- SCSI (Small Computer System Interface)
    - 7~15개 연결 가능
    - 자체 버스, 컨트롤러로 DMA 사용
- EIDE (Enhanced Integrated Device Electronics)
    - 컴퓨터 <-> 대용량 저장장치 표준 인터페이스
    - DMA 지원
    - HDD, CD-ROM 연결로 쓰였었음
- IEEE (Institute of Electrical and Electronics Engineering)
    - 고속 직렬 인터페이스
    - 동영상 편집에 필수였음
- Slot
    - ISA -> VESA -> EISA
    - PCI
        - 요즘 대부분 슬롯 인터페이스
    - 그래픽 가속 포트 (AGP)
        - 고속 그래픽 데이터 처리
        - x1 x2 x4 8

## 인터페이스 연결 방식에 따른 분류
- ATA
    - HDD, CD-ROM 등 저장장치 인터페이스
    - 40핀의 병렬 케이블
- Serial ATA
    - 직렬 형태의 ATA