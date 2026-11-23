# 재실·외출 모드 연동 스마트 홈

ATmega128(16 MHz) 하나로 도어락, 온도별 팬, 조도별 조명, 침입 경보를 집의 상태
(재실 / 외출 대기 / 외출·보안 / 경보)에 따라 통합 제어하는 스마트 홈. SimulIDE에서 시뮬레이션한다.

- 개발 환경: Microchip Studio (AVR-GCC, C)
- 시뮬레이션: SimulIDE (.hex 로드)
- 과제 개요: [docs/스마트홈_과제개요.pdf](docs/스마트홈_과제개요.pdf)

## 폴더 구조

```
smartHome/
├─ smart_home/      메인 과제 (기초 1 도어락 + 기초 3 쿨링 포함), .simu 회로
├─ stopwatch/       기초 2 디지털 타이머·스톱워치 (별도 회로)
├─ docs/
│  ├─ 스마트홈_과제개요.pdf
│  ├─ troubleshooting.md   트러블슈팅 기록
│  └─ captures/            시험(T1~T9) 화면·파형 캡처
└─ .gitignore
```

## 개발 순서 (단계마다 커밋)

1. `init: pin map and LCD driver`
2. `feat: keypad scan`
3. `feat: door lock with servo` (기초 1)
4. `feat: temperature fan control` (기초 3)
5. `feat: light sensor lamps`
6. `feat: home state machine`
7. `feat: uart status log`
8. `fix: ...` (트러블슈팅 기록과 연결)
