# 양봉관리 WebView APK 빌드 프로젝트

이 저장소는 `bee_care_integrated_pro.html` 단일 HTML 프로그램을 Android WebView APK로 빌드하기 위한 GitHub Actions 프로젝트입니다.

## GitHub에 올릴 때 필수 구조

저장소 첫 화면에 아래 항목이 바로 보여야 합니다.

```text
.github
app
README.md
build.gradle
settings.gradle
```

특히 아래 파일이 있어야 Actions 탭 왼쪽에 `Build Android APK` 메뉴가 생깁니다.

```text
.github/workflows/android.yml
```

## APK 빌드 방법

1. GitHub 저장소 상단의 `Actions` 클릭
2. 왼쪽 메뉴에서 `Build Android APK` 클릭
3. `Run workflow` 클릭
4. Branch가 `main`인지 확인
5. 초록색 `Run workflow` 클릭
6. 빌드 완료 후 실행 결과 화면 아래 `Artifacts`에서 `bee-care-webview-debug-apk` 다운로드
7. ZIP 압축을 풀면 `app-debug.apk`가 있습니다.

## .github 폴더가 업로드되지 않을 때

GitHub 홈페이지에서 직접 만드세요.

1. `Code` 탭
2. `Add file`
3. `Create new file`
4. 파일 이름 칸에 아래를 그대로 입력

```text
.github/workflows/android.yml
```

5. 이 프로젝트 안의 `.github/workflows/android.yml` 내용을 그대로 붙여넣기
6. `Commit changes`

## 주의

- ZIP 파일 자체를 올리지 말고 압축을 푼 뒤 내부 파일과 폴더를 올리세요.
- `app`, `.github`, `build.gradle`, `settings.gradle`이 저장소 최상단에 있어야 합니다.
- APK는 테스트용 debug APK입니다.
