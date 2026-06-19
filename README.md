# Be.Ark Landing (re-be.world)

칸 데모용 Be.Ark 홍보 단일 페이지. 의존성 0, 정적 HTML.

## 구조
- `index.html` — 랜딩 페이지 (Hero / Features / How / Download CTA)
- `dist-assets/설치 후 꼭 필독.command` — .dmg에 동봉할 macOS 설치 도우미
  (더블클릭 → 튜토리얼 출력 → `xattr -cr`로 격리 해제 → 앱 자동 실행)

## 배포 (Vercel)
정적이라 빌드 불필요. Vercel에 이 repo 연결 → Framework: **Other** → Output dir: `./` (루트).
그 다음 **re-be.world 도메인을 이 프로젝트로 이동.**

## 다운로드 링크
`index.html` 맨 아래 `DOWNLOAD_URL` 변수 한 줄만 수정하면 모든 버튼에 반영됨.
기본값 = `https://github.com/kyungsinkim-sketch/Be.Ark/releases/latest`
(Be.Ark repo가 private면 익명 다운로드 안 됨 → public release 또는 직접 .dmg 링크로 교체)

## .dmg에 .command 동봉하는 법
빌드한 .dmg 안에 `Be.Ark.app`과 `설치 후 꼭 필독.command`를 같이 넣으면,
유저가: ① .dmg 열기 → ② .command 더블클릭 → ③ 패치된 앱 실행.
(.command는 같은 폴더의 .app, /Applications, ~/Downloads, ~/Desktop 순으로 앱을 찾음)
실행 권한 유지 필요: `chmod +x "설치 후 꼭 필독.command"`
