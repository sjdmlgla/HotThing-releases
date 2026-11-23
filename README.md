# HotThing 배포 저장소

C17 / Win32로 만든 Windows 10/11 x64용 초고속 파일 이름 검색기 **HotThing**의 설치·업데이트 파일만 올리는 저장소입니다.
소스 코드는 공개하지 않습니다.

## 설치

1. [최신 릴리스](https://github.com/sjdmlgla/HotThing-releases/releases/latest)에서 `Setup_HotThing.exe`를 내려받습니다.
2. 실행하면(관리자 권한 승인) `C:\HotUtility\HotThing`(바꿀 수 있음)에 설치하고, 이미 설치되어 있으면 새 버전으로 업데이트합니다.
   HotThing은 NTFS 색인(MFT/USN)을 읽으려고 관리자 권한으로 실행됩니다.
3. 제거는 Windows 설정 → 앱 → 설치된 앱 → HotThing에서 합니다.

## 자동 업데이트

Setup으로 설치한 HotThing은 시작 1분 뒤와 실행 중 20시간마다 이 저장소의 최신 릴리스를 확인합니다.
새 버전이 있으면 알려 주고, [지금 업데이트]를 누르면 설치 파일을 내려받아 함께 올린
`Setup_HotThing.exe.sha256` 검증값과 같을 때만 실행해 새 버전으로 바꿉니다(설정과 색인은 그대로 이어 씀).
트레이 아이콘의 오른쪽 단추 메뉴 → [업데이트 확인]에서 직접 확인할 수도 있습니다.

## 검증값 확인

```
certutil -hashfile Setup_HotThing.exe SHA256
```

결과가 릴리스의 `Setup_HotThing.exe.sha256` 내용과 같아야 합니다.
