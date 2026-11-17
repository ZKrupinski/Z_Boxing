# Z_Boxing 개발 운영 규칙

## 개발 기준
- `main`은 확인 가능한 최신 플레이 가능한 버전. 대규모 수정을 바로 덮어쓰지 말고 QA 후 반영.
- `index.html`은 사용자가 실행할 최신 버전.
- 별도의 버전별 폴더나 HTML 백업본은 만들지 않는다. 최신 실행판은 루트 `index.html` 하나로 관리하고 `docs/CHANGELOG.md`를 갱신한다.
- 변경 시 먼저 새 프레임 데이터/애니메이션/로직 충돌 테스트를 확인한다.

## QA 우선순위
1. 키보드 포커스와 터치 입력이 채팅/브라우저로 새지 않는가
2. 프레임 데이터와 실제 hitbox/hurtbox가 정확한가
3. 넉백, 로프, 푸시박스가 관통·텔레포트하지 않는가
4. KO·다운·기상 시 플래시/잔상/이전 공격 상태가 리셋되는가
5. 모바일 가로 고정 / 해상도 대응 / 지속 성능

## 배포
GitHub > Settings > Pages > Build and deployment > Deploy from a branch > main / root 선택. 설정 이후 공개 URL은 보통 `https://zkrupinski.github.io/Z_Boxing/` 형식이다. **실제 활성화와 배포 성공 여부는 별도 확인 필요.**

## 파일 규칙
- 실행 HTML은 루트 `index.html` 하나만 유지하며 변경 이력은 Git 기록에서 확인
- 메인 실행판은 `index.html` 유지
- 에셋을 외부 분리할 경우 HTML과 같은 기준 폴더에서 상대 경로로 로드되도록 검증
- 정식 리소스와 테스트·임시 원화는 구분
