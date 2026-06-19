# industrial_patrol_robot Embedded Control
SLAM 및 CAN 네트워크 기반 산업용 순찰 로봇 - STM32/CAN 임베디드 제어 파트

## 프로젝트 개요

본 프로젝트는 공사장 및 작업장 내 안전 관리를 위해 자율 순찰 로봇을 개발한 팀 프로젝트입니다.  
로봇은 LiDAR 기반 SLAM을 통해 주행 환경을 인식하고, YOLO 기반 객체 인식을 통해 작업자의 안전장비 착용 여부를 감지합니다.

본 레포지토리는 전체 팀 프로젝트 중 제가 담당한 **STM32 기반 임베디드 제어 파트**를 중심으로 정리한 문서입니다.

## 담당 역할

저는 본 프로젝트에서 임베디드 제어 및 하드웨어 연동 파트를 담당했습니다.

- STM32F429ZI 기반 Function Control Node 개발
- CAN Bus 기반 제어 메시지 송수신 구조 구현
- Raspberry Pi 5와 STM32 제어 보드 간 시스템 연동
- LED, Buzzer, RGB LED, Photo Sensor, Servo Motor 제어
- GPIO, ADC, PWM, CAN Peripheral 설정 및 제어
- Servo Motor PWM 출력 불안정 문제 분석
- 전원 공급 및 GND 연결 문제 분석을 통한 하드웨어 안정화

## 사용 기술

### Embedded

- STM32F429ZI
- STM32F446
- STM32CubeIDE
- C
- HAL Driver
- GPIO
- ADC
- PWM
- CAN Communication

### Robot System

- Raspberry Pi 5
- ROS2
- LiDAR
- RealSense D435
- YOLOv5
- OpenCV

### Hardware

- Servo Motor
- Buzzer
- RGB LED
- Photo Sensor
- Ultrasonic Sensor
- CAN Transceiver

## 시스템 구조

추후 시스템 구조도를 추가할 예정입니다.

```text
Raspberry Pi 5
 ├── ROS2
 ├── SLAM
 ├── YOLO Object Detection
 └── CAN Communication
        ↓
STM32F429ZI
 ├── LED Control
 ├── Buzzer Control
 ├── RGB LED Control
 ├── Photo Sensor ADC
 └── Servo Motor PWM
        ↓
STM32F446
 └── Motor Control
```

### 원본 레포지토리
https://github.com/sanghyeon-222/site_inspection_robot
