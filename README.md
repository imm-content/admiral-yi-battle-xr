# 이순신 장군의 바다 — 판옥선 XR

**넓어진 울돌목 바다·전방 접근 함대·스마트폰 브라우저 AR 체험**

1597년 명량해전을 소재로 한 **스마트폰·PC용 역사 교육 XR 체험**입니다. 판옥선과 이순신 장군, 일본군 아타케부네 3척을 3D로 표시하고, 한국어 내레이션·대포 소리·포격·침몰과 승리 장면을 체험할 수 있습니다. 실제 전투의 개별 함선 배치나 교전 순서를 정확히 복원한 자료가 아닌 **교육용 축약 연출**입니다.

## 체험하기

- **공개 페이지:** https://imm-content.github.io/admiral-yi-battle-xr/
- **GitHub 저장소:** https://github.com/imm-content/admiral-yi-battle-xr

## 주요 기능

- **3D 항해:** 판옥선이 울돌목 바다 위로 다가오는 장면, 화면 회전·확대·축소
- **일본군 함선 등장:** 아타케부네 3척의 접근 장면과 방향 전환
- **포격 및 침몰:** 대포음, 포탄, 포연, 물보라와 적선 3척의 순차 침몰
- **역사 해설:** 한국어 자막과 기기 내장 음성 합성(TTS)
- **카메라 AR:** 지원되는 Android Chrome·WebXR 기기에서 실제 공간에 바다와 함선 배치

## 파일 구성

```text
admiral-yi-battle-xr/
├── index.html                 # XR 체험 화면 및 애니메이션
├── uldolmok-sea-texture.png   # 울돌목 바다 질감 (필수)
├── japanese_warship.glb       # 일본군 아타케부네 모델 (필수)
└── README.md                  # 프로젝트 설명
```

`index.html`은 다음 **외부 모델 2개**를 개인 계정의 별도 저장소에서 불러옵니다.

- 판옥선: https://imm-content.github.io/admiral-yi-history-xr/Sketchfab_panokseon.glb
- 이순신 장군: https://imm-content.github.io/admiral-yi-history-xr/admiral-yi-sunsin.glb

따라서 `imm-content/admiral-yi-history-xr` 저장소에 위 두 모델 파일이 있고 GitHub Pages에서 접근 가능해야 합니다. 이 저장소에는 `japanese_warship.glb`와 `uldolmok-sea-texture.png`를 그대로 유지해야 합니다.

## 사용 방법

1. 공개 페이지를 열고 모델 로딩이 완료될 때까지 기다립니다.
2. **3D 항해 연출 시작**을 눌러 판옥선의 접근을 봅니다.
3. **일본군 함선 등장**을 누른 다음 **판옥선 포격 시작**을 누릅니다.
4. 역사 해설·내레이션·대포 소리 버튼을 조절하거나 회전·확대·축소를 체험합니다.
5. AR 지원 기기에서는 **카메라 AR 시작 → 이 위치에 바다 배치** 순서로 체험합니다.

## 실행 환경 및 참고사항

- PC 및 스마트폰의 최신 브라우저에서 3D 미리보기 이용 가능
- 카메라 AR은 HTTPS와 WebXR `immersive-ar`·hit-test를 지원하는 기기 및 브라우저에서만 작동
- 음성 해설은 브라우저·기기에 한국어 TTS가 있어야 정상 재생
- Three.js는 jsDelivr CDN에서 로드하므로 인터넷 연결 필요
- 모델 로딩에 실패하면 **파일명 대소문자**, GitHub Pages 배포 상태 및 외부 모델 URL을 확인

> **역사적 유의사항:** 화면 속 일본군 함선 3척은 교육용 축약 표현입니다. 실제 명량해전의 전체 함대 규모나 전투 순서를 뜻하지 않습니다.
