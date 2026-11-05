# homepage/site

Export Agent 파일럿 공개 사이트의 정적 파일 묶음이다. `index.html`(소개), `guide.html`(고객 가이드), `request.html`(접근 요청)과 `portal-url.txt`로 이루어진다.

Hoon이 승인하면 이 폴더를 그대로 GitHub Pages 또는 Cloudflare Pages에 올린다. 빌드 과정은 없고 `.nojekyll`은 GitHub Pages가 파일을 그대로 서빙하게 한다.

Cloudflare 터널을 재시작해 포털 주소가 바뀌면 `portal-url.txt`의 한 줄을 새 `https://...trycloudflare.com` 주소로 바꾸고 다시 배포한다. `request.html`은 이 파일을 읽어 "Open the request form" 버튼을 `<주소>/request-access`로 연결하므로 HTML은 고치지 않아도 된다.

이 폴더의 페이지는 아무 데이터도 수집하지 않는다. 폼과 업로드는 모두 포털 쪽에 있고, 여기에는 외부 스크립트가 없다(글꼴만 Google Fonts에서 불러온다).
