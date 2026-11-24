# PayKR GitHub Pages 루트 사이트 및 AdSense 심사용 파일

이 저장소는 `https://diligencefrozen.github.io/` 주소를 제공하는 **GitHub Pages 사용자 사이트 저장소**입니다.

기존 지도 앱 저장소 `diligencefrozen/PayKR`는 별도로 유지하며, 실제 앱 주소는 다음과 같습니다.

- 지도: https://diligencefrozen.github.io/PayKR/
- 온라인 브랜드 목록: https://diligencefrozen.github.io/PayKR/online.html

## 1. 업로드 방법

이 ZIP의 **내용물 전체**를 `diligencefrozen.github.io` 저장소의 `main` 브랜치 최상위(`/`)에 업로드합니다. ZIP 파일 자체를 저장소 루트에 올리는 것이 아닙니다.

기존 `README.md`는 이 파일로 교체해도 됩니다. 저장소 최상위에 반드시 `index.html`이 있어야 합니다.

## 2. GitHub Pages 설정

1. GitHub에서 `diligencefrozen/diligencefrozen.github.io` 저장소를 엽니다.
2. `Settings` → `Pages`로 이동합니다.
3. `Build and deployment`의 `Source`를 `Deploy from a branch`로 선택합니다.
4. Branch는 `main`, Folder는 `/(root)`로 선택하고 `Save`합니다.
5. `Actions` 탭에서 Pages 배포가 성공했는지 확인합니다.
6. 배포 후 다음 주소들을 직접 열어 확인합니다.
   - https://diligencefrozen.github.io/
   - https://diligencefrozen.github.io/privacy.html
   - https://diligencefrozen.github.io/terms.html
   - https://diligencefrozen.github.io/ads.txt
   - https://diligencefrozen.github.io/robots.txt
   - https://diligencefrozen.github.io/sitemap.xml

GitHub Pages는 사용자 사이트 저장소 이름이 `<username>.github.io`인 경우 해당 도메인의 루트 사이트로 게시합니다. 기존 `PayKR` 프로젝트 사이트 저장소는 별도 저장소이므로 `/PayKR/` 경로를 유지합니다.

## 3. 포함 파일

- `index.html`: PayKR 소개·사용 방법·FAQ가 포함된 루트 홈페이지. AdSense 코드 스니펫 포함.
- `about.html`: 서비스 소개
- `guide.html`: 지도 및 온라인 목록 사용 가이드
- `privacy.html`: 한국어 개인정보처리방침
- `terms.html`: 한국어 이용약관
- `contact.html`: 정보 수정 및 문의 안내
- `en/`: 위 페이지의 영어 버전
- `ads.txt`: 게시자 ID `pub-3313505766731703`
- `robots.txt`: 크롤러 허용 및 sitemap 경로
- `sitemap.xml`: 루트 사이트와 기존 `/PayKR/` 앱의 주요 URL
- `404.html`: 사용자 정의 오류 페이지
- `assets/style.css`: 공통 반응형 스타일

## 4. AdSense 연결

루트 홈페이지 `<head>`에 다음 AdSense 코드가 포함되어 있습니다.

```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3313505766731703"
     crossorigin="anonymous"></script>
```

- 게시자 ID: `ca-pub-3313505766731703`
- `ads.txt`는 `https://diligencefrozen.github.io/ads.txt`에서 열려야 합니다.
- 현재 패키지에는 **실제 광고 슬롯 코드(`data-ad-slot`)를 넣지 않았습니다.** 사이트 등록/소유권 확인용 코드와 실제 광고 단위는 서로 다릅니다.
- 사이트가 승인되고 광고 단위를 생성한 후 실제 광고를 배치합니다.
- 코드가 들어갔다고 해서 사이트가 자동 승인되는 것은 아닙니다. AdSense에서 사이트 검토를 별도로 요청해야 합니다.

AdSense 사이트 입력란에는 URL 경로를 붙이지 말고 `diligencefrozen.github.io`를 사용합니다. Google은 일반 사이트 등록 시 경로가 없는 표준 도메인을 요구하며, 사이트 소유권 확인 후 정책 검토를 진행합니다.

## 5. 업로드 전 반드시 확인할 점

1. `privacy.html`에는 현재 확인된 기존 PayKR 지도 코드의 IP 위치 대체 동작을 사실대로 공개했습니다. 현재 앱 코드에는 GPS 실패 시 `ipapi.co`를 호출하는 로직이 있습니다. 사용자가 요청한 대로 Codex가 이 기능을 제거해 배포한 뒤에는 한국어·영어 개인정보처리방침의 해당 문단을 실제 동작에 맞게 수정해야 합니다.
2. 문의는 기존 PayKR GitHub Issues를 연결했습니다. GitHub Issues는 공개될 수 있으므로 개인정보나 금융정보를 올리지 말라는 안내를 넣었습니다.
3. 운영자 실명, 사업자 주소, 공개 문의 이메일은 임의로 만들지 않았습니다. 개인정보 관련 공식 연락처를 별도로 공개할 계획이면 해당 정보를 확인해 정책에 추가합니다.
4. 이 패키지는 사이트 구조와 기본 정보 페이지를 제공하지만, AdSense 승인 자체를 보장하지 않습니다. Google은 사이트의 고유하고 유용한 콘텐츠 및 프로그램 정책 준수 여부를 별도로 검토합니다.
5. 루트 홈페이지는 단순 자동 리다이렉트가 아닙니다. 실제 소개·가이드·FAQ 콘텐츠를 제공하고 사용자가 지도 앱으로 이동하도록 구성했습니다.

## 6. 최종 점검 체크리스트

- [ ] 저장소 루트에 `index.html`이 업로드됨
- [ ] GitHub Pages가 `main` / `/(root)`로 배포됨
- [ ] `https://diligencefrozen.github.io/`에서 홈페이지가 열림
- [ ] `/PayKR/` 지도 앱이 계속 열림
- [ ] `/PayKR/online.html` 온라인 브랜드 목록이 계속 열림
- [ ] `/privacy.html`, `/terms.html`, `/contact.html`가 열림
- [ ] `/ads.txt`에 게시자 ID가 표시됨
- [ ] `/robots.txt`가 루트 sitemap을 가리킴
- [ ] `/sitemap.xml`이 정상 XML로 열림
- [ ] AdSense에서 사이트 소유권 확인 및 검토 요청
- [ ] GPS IP fallback 제거 후 개인정보처리방침 문구 업데이트
