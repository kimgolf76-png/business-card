# Business Card (React Native)

간단한 NFC 명함 교환 앱(React Native).

## 개요
이 프로젝트는 React Native + react-native-nfc-manager를 사용하여 iOS/Android 양쪽에서 NFC 태그를 읽고(및 쓰기) 명함 정보를 교환하는 예제 앱입니다.

## 빠른 시작
1. 프로젝트 생성 (권장)
   ```bash
   npx react-native init business_card_app
   cd business_card_app
   ```
2. 의존성 설치
   ```bash
   npm install react-native-nfc-manager
   cd ios && pod install && cd ..
   ```
3. iOS 설정 (Xcode)
   - Xcode에서 ios/ 폴더의 workspace를 열기: `open ios/business_card_app.xcworkspace`
   - Signing & Capabilities → + Near Field Communication Tag Reading 추가
   - Info.plist에 `NFCReaderUsageDescription` (Privacy - NFC Scan Usage Description) 키를 추가하고 설명 텍스트를 입력
4. Android 설정
   - `android/app/src/main/AndroidManifest.xml`에 NFC 권한/feature 추가 (README 예시 참고)
   - minSdkVersion >= 19 권장
5. 실행 (물리 기기 필요)
   - Android: `npx react-native run-android`
   - iOS: `npx react-native run-ios`

## 기능
- NFC 태그 스캔(읽기)
- NDEF 텍스트/URI 읽기
- (선택) 명함 정보(vCard 등)를 NFC에 쓰기

## 파일 구조(권장)
- App.js            # 앱 진입점 및 예제 UI
- index.js
- package.json
- android/ ios/     # 플랫폼 네이티브 코드
- .gitignore

## 라이선스
All Rights reserved by LAB82, company, Korea
