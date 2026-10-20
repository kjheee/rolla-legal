# Rolla 공개 정책·지원 사이트

공개 정책과 고객지원 안내만 관리한다. 앱 소스·키·개인정보·운영 로그를 이 저장소에 넣지 않는다. 앱 저장소의 `docs/legal`은 과거 초안이며 이 저장소가 공개 문서 원본이다.

## 공개 문서와 버전

기준 주소: https://kjheee.github.io/rolla-legal/

- `/terms/`: 이용약관, 2026-10-20 시행
- `/privacy/`: 개인정보 처리방침, 2026-10-20 시행
- `/community/`: 금지 콘텐츠·아동 안전·신고·제재·이의제기
- `/support/`: 운영자·개인정보 책임자·지원 이메일
- `/delete-account/`: 앱 내 삭제 및 이메일 삭제 요청

GitHub Pages의 main 루트 Jekyll 배포를 사용한다. 앱의 `LEGAL_VERSION`과 신규 가입 RPC는 `2026-10-20`을 사용하도록 맞춘다. 배포된 앱에 새 버전이 포함되는 시점은 앱 빌드 배포 시점이다. 과거 가입자의 동의 버전·시각은 덮어쓰지 않는다.

## 이번 문서 정리의 판단 근거

- Supabase의 주요 DB·Auth·Storage는 확인한 서울 리전을 기재한다. 서버 함수·로그·지원·재위탁까지 전부 국내에서 처리된다고 확대 해석하지 않는다. 회사 소재지와 실제 저장 위치도 구분한다.
- Expo·APNs·FCM은 실제 푸시 전달 경로를 기재한다. 메시지의 전달 대기 기간과 토큰·설치 ID의 보관 기준을 구분한다. 공개 자료에 일률적인 토큰 보관 일수가 없으면 그 사실과 요청 경로를 설명하며 임의로 기한을 만들지 않는다.
- Gmail은 이용자가 선택한 이메일 문의 수신·회신과 보관에 한정한다. 앱 문의의 자동 전달 채널로 오인하지 않게 한다.
- GitHub Pages의 방문 접속 정보는 공급자의 직접 수집으로 안내한다. 회원 DB·기록·사진을 GitHub에 제공하는 항목으로 분류하지 않는다. 해외 사업자의 직접 수집과 국내 처리자의 국외 이전은 구분한다는 개인정보보호위원회 안내를 참고했다.
- 계약 이행에 필요한 처리위탁·보관의 적용 근거와 이용자 선택을 공개 문서에 기재했다. OS 알림 권한이나 일반 약관 동의를 별도 국외 이전 동의로 보지 않는다.
- Discord는 신규 이용자 정보를 전송하지 않는다. 고정된 접수 문구만 전달하며 과거 사본은 파기 대상에 포함한다.

공급자 전체 내부 시스템 감사나 모든 백업의 물리적 파기 증명까지 출시 선행 작업으로 두었던 범위는 철회한다. 이 문서는 실제 구성과 공개 자료를 정리한 것이며 공급자의 비공개 사실을 확인했거나 법률 검토·인증을 받았다는 뜻은 아니다. 처리 방식·공급자·플랜을 바꾸면 해당 변경 범위를 다시 확인한다.

## 운영 기준

운영자·개인정보 책임자는 김정희이며 지원 이메일은 `heehee2302@gmail.com`이다. 앱에서는 문의 폼을 제공하고 이메일 주소는 공개 고객지원 페이지에 안내한다.

기존 계정 삭제 기능과 운영자의 수동 처리로 시작한다. 별도 자동 파기 시스템·관리자 도구 개발이나 전수 장애 시험을 선행 조건으로 두지 않는다.

1. 매일 미처리 신고·문의를 확인한다. 신고는 접수 후 24시간 내 검토 시작을 목표로 한다.
2. 처리 완료 시 비공개 대장에 대상 ID·완료 시각·파기 기한·저장 위치·결과를 기록한다. 원문·사진·비밀번호·토큰을 공개 저장소에 남기지 않는다.
3. 신고·문의 DB 자료·첨부·관련 이메일 및 과거 Discord 개인정보 사본은 처리 완료 후 1년 이내 파기한다. 탈퇴 관련 개인정보와 더 이상 필요하지 않은 자료는 먼저 삭제한다.
4. 수동 백업은 생성 후 30일 이내 파기한다. 탈퇴자 정보는 앞당겨 제거하며 개별 제거가 어렵다면 해당 백업을 폐기하거나 정리한 사본으로 교체한다.
5. 각 저장 위치의 삭제 결과를 확인한다. 실패는 재처리하고 완료 전에는 삭제됐다고 안내하지 않는다. 복원 시 이미 삭제한 계정 정보가 되살아나지 않도록 확인한다.

1년·30일은 승인된 최대 운영 기간으로, 그 기간 동안 반드시 보관해야 한다는 뜻이 아니다. 실제 데이터 삭제는 범위 확인과 필요한 승인을 거쳐 수행한다. 코드·문서 변경으로 과거 외부 사본이 삭제된 것으로 보지 않는다.

## 적용 및 검증 범위

- Supabase 서울 리전·Free 플랜, 인증 감사 로그 DB 기록 꺼짐을 확인했다. API·DB 로그 1일, 인증 감사 로그 1시간은 공식 플랜 기준이다.
- Discord의 개인정보 없는 알림은 worker와 DB 마이그레이션을 운영 서버에 배포했다. 운영 함수 확인과 로컬 회귀 테스트를 수행했다. 사용자가 Discord 알림 수신을 확인했다고 답했으며 에이전트가 실기기 전체 흐름을 확인했다는 뜻은 아니다.
- 사용자는 신고·차단·탈퇴·문의 수신 및 정책 URL 등록을 확인했다고 답했다. 스토어 콘솔의 현재 모든 항목이 완료됐다는 뜻은 아니다.
- 이번 문서 정리는 기존 처리 방식의 구체화와 Discord 전송 축소다. 공개 처리방침에 변경 안내를 게시한다. 새로운 처리 목적이나 별도 동의가 필요한 전송을 추가할 때에는 그에 맞는 고지·동의 절차를 먼저 마련한다.
- 대표적인 테스트 계정으로 서버 삭제·외부 사본 파기 경로를 확인하는 것은 권장 운영 점검이다. 실제 기한이나 삭제 요청이 도래하면 파기 절차는 수행해야 한다.

문서 공개·앱 소스 반영·배포 앱 업데이트·스토어 심사 완료는 각각 구분하여 보고한다.

## 확인한 공식 자료

- [개인정보보호위원회 국외 이전 안내](https://pipc.go.kr/np/default/page.do?mCode=D060040000)
- [Supabase 데이터 위치](https://supabase.com/docs/guides/security/gdpr-compliance) · [플랜](https://supabase.com/pricing) · [DPA](https://supabase.com/legal/customer-resources/data-processing-addendum)
- [Expo 개인정보 설명](https://expo.dev/privacy-explained) · [푸시 FAQ](https://docs.expo.dev/push-notifications/faq/) · [재위탁 목록](https://expo.dev/privacy/subprocessors)
- [Apple 개인정보 방침](https://www.apple.com/legal/privacy/en-ww/) · [APNs 전달](https://developer.apple.com/documentation/usernotifications/sending-notification-requests-to-apns)
- [Firebase 처리·보관 기준](https://firebase.google.com/support/privacy) · [FCM 메시지 수명](https://firebase.google.com/docs/cloud-messaging/customize-messages/setting-message-lifespan)
- [Google 개인정보 방침](https://policies.google.com/privacy?hl=ko) · [보관 기준](https://policies.google.com/technologies/retention?hl=ko)
- [GitHub Pages 접속 정보](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection) · [개인정보 방침](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
