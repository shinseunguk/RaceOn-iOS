# 🏃🏻 런닝 경쟁 앱 RaceOn

![표지 이미지](https://github.com/user-attachments/assets/5614261a-c203-4533-8ff3-18335801b50c)


- 배포 URL : https://apps.apple.com/kr/app/raceon/id6739800853

<br>

## 프로젝트 소개

- RaceOn은 실시간으로 친구들과 경쟁하며 달리기를 즐길 수 있는 런닝 경쟁 앱입니다.
사용자는 GPS 기반으로 자신의 달리기 경로와 속도를 확인 할 수 있습니다.

<br>

## 팀원 구성

<div align="center">

| **iOS / 신승욱** | **iOS / 정진우** | **Android / 이유호** | **Android / 박희원** | **Backend / 정민욱** | **Backend / 이상협** |
| :------: | :------: | :------: | :------: | :------: | :------: |
| [<img src="https://avatars.githubusercontent.com/u/69791286?v=4" height=100 width=100> <br/> @shinseunguk](https://github.com/shinseunguk) | [<img src="https://avatars.githubusercontent.com/u/83794512?v=4" height=100 width=100> <br/> @jinwoojung97](https://github.com/jinwoojung97) | [<img src="https://avatars.githubusercontent.com/u/57080476?v=4" height=100 width=100> <br/> @YuhoLee](https://github.com/YuhoLee) | [<img src="https://avatars.githubusercontent.com/u/80496838?v=4" height=100 width=100> <br/> @HeewonP825](https://github.com/HeewonP825) | [<img src="https://avatars.githubusercontent.com/u/46997074?v=4" height=100 width=100> <br/> @J-MU](https://github.com/J-MU) | [<img src="https://avatars.githubusercontent.com/u/75459370?v=4" height=100 width=100> <br/> @723poil](https://github.com/723poil) |



</div>

<br>

## 1. 개발 환경

- iOS : Xcode
- Android : Android Studio
- Back-end : InteliJ, Spring, 
- 버전 및 이슈관리 : Github, Github Issues, Github Project
- 협업 툴 : Discord, Notion, Github Wiki
- 디자인 : [Figma](https://www.figma.com/design/xzMBGfaope5mtYuiON81ru/RACE-ON?node-id=9-3&p=f&t=99G1AibO0m8YYGMl-0)
- [커밋 컨벤션](https://github.com/RaceOnProject/RaceOn-iOS/wiki/Commit-Convention)
- [코드 리뷰 컨벤션](https://github.com/RaceOnProject/RaceOn-iOS/wiki/Code-Review-Convention)
- 코드 컨벤션: SwiftLint
<br>

## 2. 채택한 개발 기술과 브랜치 전략

### SwiftUI, Combine

- **반응형 UI**
    - SwiftUI의 선언형 문법을 활용하여 직관적인 UI 개발이 가능합니다.
    - Combine을 사용해 데이터 흐름을 관리하며, 비동기 이벤트 처리를 효과적으로 수행할 수 있습니다.
- **상태 관리**
    - `@State`, `@Binding` 등을 활용하여 컴포넌트 간 상태 관리를 효율적으로 구현했습니다.
    - 비즈니스 로직과 UI를 분리하여 유지보수성을 높였습니다.

### Tuist

- **모듈화된 프로젝트 관리**
    - Tuist를 사용하여 프로젝트를 구성함으로써, 의존성을 명확하게 관리하고 빌드 속도를 개선했습니다.
- **자동화된 프로젝트 설정**
    - 새로운 모듈 추가 시 Tuist 스크립트를 활용해 일관된 프로젝트 구조를 유지할 수 있도록 했습니다.
- **Xcode 프로젝트 변경 사항 버전 관리**
    - `.xcodeproj` 파일을 직접 수정하는 대신 Tuist를 이용해 Git 충돌을 최소화하고 협업을 원활하게 진행할 수 있도록 했습니다.
-  **기능별 모듈화**
    - 기능별로 프로젝트를 나눠 테스트 및 TestFlight 업로드를 더욱 더 용이하게 만들었음.

### TCA (The Composable Architecture)

- **일관된 상태 관리**
    - SwiftUI와 궁합이 좋은 TCA를 사용하여 상태를 명확하게 정의하고 관리했습니다.
- **의존성 관리와 테스트 용이성**
    - Reducer를 기반으로 한 명확한 액션 처리와 사이드 이펙트 관리가 가능합니다.
    - 각 기능별로 독립적인 모듈을 구성하여 유닛 테스트를 용이하게 했습니다.
- **확장성과 유지보수성**
    - 기능 단위로 분리하여 확장성을 높이고, 기능 추가 시 기존 코드에 영향을 최소화하도록 설계했습니다.

### Clean Architecture

- **구조적 설계**
    - 의존성 역전을 통해 도메인 로직이 프레젠테이션 및 데이터 계층에 종속되지 않도록 설계했습니다.
    - 유지보수성과 테스트 용이성을 고려하여 각 모듈을 분리했습니다.
- **모듈화**
    - 기능별로 모듈을 나누어 코드의 재사용성을 높이고 독립적인 개발이 가능하도록 구성했습니다.
    - App, Presentation, Domain, Data, Shared 등의 모듈로 분리하여 역할을 명확히 했습니다.
- **의존성 관리**
    - 각 계층 간 의존성을 최소화하고 인터페이스를 활용하여 결합도를 낮추었습니다.

### 브랜치 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다.
    - **feature** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge/rebase 후 각 브랜치를 삭제해주었습니다.

<br>

## 3. 프로젝트 구조

```
.
├── DemoApps
│   ├── Friend
│   │   ├── Derived
│   │   │   └── Sources
│   │   │       └── TuistBundle+FriendDemoApp.swift
│   │   ├── FriendDemoApp.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── FriendDemoApp.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Project.swift
│   │   ├── Resources
│   │   │   └── LaunchScreen.storyboard
│   │   ├── Sources
│   │   │   └── App.swift
│   │   ├── Tests
│   │   │   └── Dummy.swift
│   │   └── build
│   │       └── XCBuildData
│   │           ├── 1241ae30cddb5fc4584e99ceb16cdc57.xcbuilddata
│   │           │   ├── build-request.json
│   │           │   ├── description.msgpack
│   │           │   ├── manifest.json
│   │           │   ├── target-graph.txt
│   │           │   └── task-store.msgpack
│   │           ├── 43dc15a0bce8d510f348c8cd92d962e6.xcbuilddata
│   │           │   ├── build-request.json
│   │           │   ├── description.msgpack
│   │           │   ├── manifest.json
│   │           │   ├── target-graph.txt
│   │           │   └── task-store.msgpack
│   │           ├── c88b265e6bbb5a36e1754b9b35192f65.xcbuilddata
│   │           │   ├── build-request.json
│   │           │   ├── description.msgpack
│   │           │   ├── manifest.json
│   │           │   ├── target-graph.txt
│   │           │   └── task-store.msgpack
│   │           └── ddc8471b377ba4e4883257979b3d379c.xcbuilddata
│   │               ├── build-request.json
│   │               ├── description.msgpack
│   │               ├── manifest.json
│   │               ├── target-graph.txt
│   │               └── task-store.msgpack
│   ├── Running
│   │   ├── Derived
│   │   │   └── Sources
│   │   │       └── TuistBundle+RunningDemoApp.swift
│   │   ├── Project.swift
│   │   ├── Resources
│   │   │   └── LaunchScreen.storyboard
│   │   ├── RunningDemoApp.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── RunningDemoApp.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Sources
│   │   │   └── App.swift
│   │   └── Tests
│   │       └── Dummy.swift
│   └── Setting
│       ├── Derived
│       │   └── Sources
│       │       └── TuistBundle+SettingDemoApp.swift
│       ├── Project.swift
│       ├── Resources
│       │   └── LaunchScreen.storyboard
│       ├── SettingDemoApp.xcodeproj
│       │   ├── project.pbxproj
│       │   ├── project.xcworkspace
│       │   │   └── contents.xcworkspacedata
│       │   ├── xcshareddata
│       │   │   └── xcschemes
│       │   │       └── SettingDemoApp.xcscheme
│       │   └── xcuserdata
│       │       └── incross0915.xcuserdatad
│       │           └── xcschemes
│       │               └── xcschememanagement.plist
│       ├── Sources
│       │   └── App.swift
│       └── Tests
│           └── Dummy.swift
├── Derived
│   ├── InfoPlists
│   │   ├── RaceOn-Info.plist
│   │   └── RaceOnTests-Info.plist
│   └── Sources
│       ├── TuistAssets+RaceOn.swift
│       └── TuistBundle+RaceOn.swift
├── Gemfile
├── Gemfile.lock
├── Makefile
├── Plugins
│   └── UtilityPlugin
│       ├── Package.swift
│       ├── Plugin.swift
│       ├── ProjectDescriptionHelpers
│       │   ├── Dependencies+Module.swift
│       │   ├── Dependencies+SPM.swift
│       │   ├── LocalHelper.swift
│       │   ├── Project+Configuration.swift
│       │   ├── Project+Extensions.swift
│       │   ├── Project+Script.swift
│       │   ├── Project+Setting.swift
│       │   └── TargetScript+Extension.swift
│       └── Sources
│           └── tuist-my-cli
│               └── main.swift
├── Projects
│   ├── App
│   │   ├── App.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       ├── App.xcscheme
│   │   │   │       └── RaceOnTests.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── App.xcworkspace
│   │   │   ├── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   ├── IDEWorkspaceChecks.plist
│   │   │   │   ├── WorkspaceSettings.xcsettings
│   │   │   │   ├── swiftpm
│   │   │   │   │   └── configuration
│   │   │   │   └── xcschemes
│   │   │   │       └── App-Workspace.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Derived
│   │   │   └── InfoPlists
│   │   │       ├── App-Info.plist
│   │   │       └── RaceOnTests-Info.plist
│   │   ├── Resources
│   │   └── Tests
│   ├── Data
│   │   ├── Data.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Data.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   └── Resources
│   ├── Domain
│   │   ├── Domain.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Domain.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Resources
│   │   └── Sources
│   ├── Presentation
│   │   ├── Derived
│   │   ├── Presentation.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Presentation.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Resources
│   │   └── Sources
│   └── Shared
│       ├── Resources
│       ├── Shared.xcodeproj
│       │   ├── project.pbxproj
│       │   ├── project.xcworkspace
│       │   │   └── contents.xcworkspacedata
│       │   ├── xcshareddata
│       │   │   └── xcschemes
│       │   │       └── Shared.xcscheme
│       │   └── xcuserdata
│       │       └── incross0915.xcuserdatad
│       │           └── xcschemes
│       │               └── xcschememanagement.plist
│       └── Sources
├── README.md
├── RaceOn
│   ├── App
│   │   ├── App.entitlements
│   │   ├── Derived
│   │   │   ├── Entitlements
│   │   │   │   └── RaceOn.entitlements
│   │   │   └── Sources
│   │   │       ├── TuistAssets+RaceOn.swift
│   │   │       ├── TuistBundle+RaceOn.swift
│   │   │       └── TuistPlists+RaceOn.swift
│   │   ├── Project.swift
│   │   ├── RaceOn.entitlements
│   │   ├── RaceOn.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   ├── contents.xcworkspacedata
│   │   │   │   ├── xcshareddata
│   │   │   │   │   └── swiftpm
│   │   │   │   │       └── configuration
│   │   │   │   └── xcuserdata
│   │   │   │       └── incross0915.xcuserdatad
│   │   │   │           └── UserInterfaceState.xcuserstate
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── RaceOn.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Resources
│   │   │   ├── Assets.xcassets
│   │   │   │   ├── AccentColor.colorset
│   │   │   │   │   └── Contents.json
│   │   │   │   ├── AppIcon.appiconset
│   │   │   │   │   ├── Contents.json
│   │   │   │   │   ├── Icon-Dark-1024x1024.png
│   │   │   │   │   ├── Icon-Light-1024x1024.png
│   │   │   │   │   └── Icon-Tinted-1024x1024.png
│   │   │   │   ├── Contents.json
│   │   │   │   ├── Splash
│   │   │   │   │   ├── Contents.json
│   │   │   │   │   └── SplashLogo.imageset
│   │   │   │   │       ├── Contents.json
│   │   │   │   │       ├── Group 238.png
│   │   │   │   │       ├── Group 238@2x.png
│   │   │   │   │       └── Group 238@3x.png
│   │   │   │   ├── appleLogo.imageset
│   │   │   │   │   ├── Apple Logo.png
│   │   │   │   │   ├── Apple Logo@2x.png
│   │   │   │   │   ├── Apple Logo@3x.png
│   │   │   │   │   └── Contents.json
│   │   │   │   ├── kakaoLogo.imageset
│   │   │   │   │   ├── Contents.json
│   │   │   │   │   ├── Kakao.png
│   │   │   │   │   ├── Kakao@2x.png
│   │   │   │   │   └── Kakao@3x.png
│   │   │   │   ├── loginMainImage1.imageset
│   │   │   │   │   ├── Contents.json
│   │   │   │   │   ├── Frame 1272629363.png
│   │   │   │   │   ├── Frame 1272629363@2x.png
│   │   │   │   │   └── Frame 1272629363@3x.png
│   │   │   │   └── loginMainImage2.imageset
│   │   │   │       ├── Contents.json
│   │   │   │       ├── Group 241.png
│   │   │   │       ├── Group 241@2x.png
│   │   │   │       └── Group 241@3x.png
│   │   │   ├── GoogleService-Info.plist
│   │   │   └── LaunchScreen.storyboard
│   │   ├── Sources
│   │   │   ├── App.swift
│   │   │   ├── AppDelegate.swift
│   │   │   └── SceneDelegate.swift
│   │   └── Tests
│   │       └── Test.swift
│   ├── Data
│   │   ├── Data.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Data.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Project.swift
│   │   ├── Sources
│   │   │   ├── API
│   │   │   │   ├── Auth
│   │   │   │   │   └── AuthAPI.swift
│   │   │   │   ├── Friend
│   │   │   │   │   └── FriendAPI.swift
│   │   │   │   ├── Game
│   │   │   │   │   └── GameAPI.swift
│   │   │   │   └── Member
│   │   │   │       └── MemberAPI.swift
│   │   │   ├── Network
│   │   │   │   ├── APIRequestRetrier.swift
│   │   │   │   ├── NetworkManager.swift
│   │   │   │   ├── TokenManager.swift
│   │   │   │   ├── WebSocketClient.swift
│   │   │   │   └── WebSocketManager.swift
│   │   │   └── Repositories
│   │   │       ├── Auth
│   │   │       │   └── AuthRepositoryImpl.swift
│   │   │       ├── Friend
│   │   │       │   └── FriendRepositoryImpl.swift
│   │   │       ├── Game
│   │   │       │   └── GameRepositoryImpl.swift
│   │   │       ├── Member
│   │   │       │   └── MemberRepositoryImpl.swift
│   │   │       └── Notification
│   │   │           └── NotificationRepositoryImpl.swift
│   │   └── Tests
│   │       └── Test.swift
│   ├── Domain
│   │   ├── Domain.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Domain.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Project.swift
│   │   ├── Sources
│   │   │   ├── Entities
│   │   │   │   ├── Auth
│   │   │   │   │   └── TokenResponse.swift
│   │   │   │   ├── Common
│   │   │   │   │   └── BaseResponse.swift
│   │   │   │   ├── Friend
│   │   │   │   │   └── FriendResponse.swift
│   │   │   │   ├── Game
│   │   │   │   │   ├── GaemMessage.swift
│   │   │   │   │   ├── GameInviteResponse.swift
│   │   │   │   │   ├── ProcessResponse.swift
│   │   │   │   │   └── StopResponse.swift
│   │   │   │   └── Member
│   │   │   │       ├── MemberCode
│   │   │   │       │   └── MemberInfo.swift
│   │   │   │       └── Profile
│   │   │   │           ├── EditProfileResponse.swift
│   │   │   │           └── ProfileImageResponse.swift
│   │   │   ├── Error
│   │   │   │   ├── NetworkError.swift
│   │   │   │   └── ServerError.swift
│   │   │   ├── Repositories
│   │   │   │   ├── Auth
│   │   │   │   │   └── AuthRepositoryProtocol.swift
│   │   │   │   ├── Friend
│   │   │   │   │   └── FriendRepositoryProtocol.swift
│   │   │   │   ├── Game
│   │   │   │   │   └── GameRepositoryProtocol.swift
│   │   │   │   ├── Member
│   │   │   │   │   └── MemberRepositoryProtocol.swift
│   │   │   │   └── Notification
│   │   │   │       └── NotificationRepositoryProtocol.swift
│   │   │   └── UseCases
│   │   │       ├── Auth
│   │   │       │   └── AuthUseCase.swift
│   │   │       ├── Friend
│   │   │       │   └── FriendUseCase.swift
│   │   │       ├── Game
│   │   │       │   ├── GameUseCase.swift
│   │   │       │   └── LocationService.swift
│   │   │       ├── Member
│   │   │       │   └── MemberUseCase.swift
│   │   │       └── Notification
│   │   │           └── CheckPushStatusUseCase.swift
│   │   └── Tests
│   │       └── Test.swift
│   ├── Presentation
│   │   ├── Derived
│   │   │   └── Sources
│   │   │       ├── TuistAssets+Presentation.swift
│   │   │       └── TuistBundle+Presentation.swift
│   │   ├── Presentation.xcodeproj
│   │   │   ├── project.pbxproj
│   │   │   ├── project.xcworkspace
│   │   │   │   └── contents.xcworkspacedata
│   │   │   ├── xcshareddata
│   │   │   │   └── xcschemes
│   │   │   │       └── Presentation.xcscheme
│   │   │   └── xcuserdata
│   │   │       └── incross0915.xcuserdatad
│   │   │           └── xcschemes
│   │   │               └── xcschememanagement.plist
│   │   ├── Project.swift
│   │   ├── Resources
│   │   │   └── Assets.xcassets
│   │   │       ├── Colors
│   │   │       │   ├── Contents.json
│   │   │       │   ├── Emphasis.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 1.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 2.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 3.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 4.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 5.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Gray 6.colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── ImageConstants.dataset
│   │   │       │   │   ├── Contents.json
│   │   │       │   │   └── ImageConstants.swift
│   │   │       │   ├── Primary (Normal).colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   ├── Primary (Pressed).colorset
│   │   │       │   │   └── Contents.json
│   │   │       │   └── Second (Normal).colorset
│   │   │       │       └── Contents.json
│   │   │       ├── Contents.json
│   │   │       └── Images
│   │   │           ├── Common
│   │   │           │   ├── Contents.json
│   │   │           │   ├── chevron-compact-right.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Vector (Stroke).png
│   │   │           │   │   ├── Vector (Stroke)@2x.png
│   │   │           │   │   └── Vector (Stroke)@3x.png
│   │   │           │   └── dividing-line.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       ├── Line 26.png
│   │   │           │       ├── Line 26@2x.png
│   │   │           │       └── Line 26@3x.png
│   │   │           ├── Contents.json
│   │   │           ├── Friend
│   │   │           │   ├── Contents.json
│   │   │           │   ├── Kebab.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Vector.png
│   │   │           │   │   ├── Vector@2x.png
│   │   │           │   │   └── Vector@3x.png
│   │   │           │   ├── Mockup Image
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Profile-0.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── Profile.png
│   │   │           │   │   │   ├── Profile@2x.png
│   │   │           │   │   │   └── Profile@3x.png
│   │   │           │   │   ├── Profile-1.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── Profile-1.png
│   │   │           │   │   │   ├── Profile@2x-1.png
│   │   │           │   │   │   └── Profile@3x-1.png
│   │   │           │   │   ├── Profile-2.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── Profile-2.png
│   │   │           │   │   │   ├── Profile@2x-2.png
│   │   │           │   │   │   └── Profile@3x-2.png
│   │   │           │   │   ├── Profile-3.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── Profile-3.png
│   │   │           │   │   │   ├── Profile@2x-3.png
│   │   │           │   │   │   └── Profile@3x-3.png
│   │   │           │   │   └── Profile-4.imageset
│   │   │           │   │       ├── Contents.json
│   │   │           │   │       ├── Profile-4.png
│   │   │           │   │       ├── Profile@2x-4.png
│   │   │           │   │       └── Profile@3x-4.png
│   │   │           │   ├── circle-check-fill.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── circle-check-1.png
│   │   │           │   │   ├── circle-check@2x-1.png
│   │   │           │   │   └── circle-check@3x-1.png
│   │   │           │   ├── circle-check.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── circle-check.png
│   │   │           │   │   ├── circle-check@2x.png
│   │   │           │   │   └── circle-check@3x.png
│   │   │           │   └── graphic-nothing.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       ├── graphic-nothing.png
│   │   │           │       ├── graphic-nothing@2x.png
│   │   │           │       └── graphic-nothing@3x.png
│   │   │           ├── Login
│   │   │           │   ├── Contents.json
│   │   │           │   ├── appleLogin.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── appleLogin.svg
│   │   │           │   ├── icon-activity.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-activity.svg
│   │   │           │   ├── icon-alarm.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-alarm.svg
│   │   │           │   ├── icon-gallery.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-gallery.svg
│   │   │           │   ├── icon-location.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-location.svg
│   │   │           │   ├── kakaoLogin.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── kakaoLogin.svg
│   │   │           │   ├── loginCenter.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── loginCenter.png
│   │   │           │   │   ├── loginCenter@2x.png
│   │   │           │   │   └── loginCenter@3x.png
│   │   │           │   └── loginLogo.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       └── loginLogo.svg
│   │   │           ├── Main
│   │   │           │   └── Contents.json
│   │   │           ├── Matching
│   │   │           │   ├── Contents.json
│   │   │           │   ├── card-10km.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── card-10km.png
│   │   │           │   │   ├── card-10km@2x.png
│   │   │           │   │   └── card-10km@3x.png
│   │   │           │   ├── card-3km.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── card-3km.png
│   │   │           │   │   ├── card-3km@2x.png
│   │   │           │   │   └── card-3km@3x.png
│   │   │           │   ├── card-5km.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── card-5km.png
│   │   │           │   │   ├── card-5km@2x.png
│   │   │           │   │   └── card-5km@3x.png
│   │   │           │   ├── graphic-invite.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── graphic-invitation.png
│   │   │           │   │   ├── graphic-invitation@2x.png
│   │   │           │   │   └── graphic-invitation@3x.png
│   │   │           │   ├── graphic-logo.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── graphic-logo.svg
│   │   │           │   ├── graphic-matching.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── graphic-matching.png
│   │   │           │   │   ├── graphic-matching@2x.png
│   │   │           │   │   └── graphic-matching@3x.png
│   │   │           │   ├── graphic-refuse.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── graphic-refuse.png
│   │   │           │   │   ├── graphic-refuse@2x.png
│   │   │           │   │   └── graphic-refuse@3x.png
│   │   │           │   ├── graphic-stop.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Group 244.png
│   │   │           │   │   ├── Group 244@2x.png
│   │   │           │   │   └── Group 244@3x.png
│   │   │           │   ├── graphic-waiting.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── graphic-waiting.png
│   │   │           │   │   ├── graphic-waiting@2x.png
│   │   │           │   │   └── graphic-waiting@3x.png
│   │   │           │   ├── icon-_setting.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-_setting.svg
│   │   │           │   ├── icon-chevron-Left.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-chevron-Left.svg
│   │   │           │   ├── icon-chevron-right.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-chevron-right.svg
│   │   │           │   ├── icon-friends.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   └── icon-friends.svg
│   │   │           │   ├── icon-lose.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Frame 1272629368.png
│   │   │           │   │   ├── Frame 1272629368@2x.png
│   │   │           │   │   └── Frame 1272629368@3x.png
│   │   │           │   ├── icon-me-lose.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Rectangle 886-2.png
│   │   │           │   │   ├── Rectangle 886@2x-2.png
│   │   │           │   │   └── Rectangle 886@3x-2.png
│   │   │           │   ├── icon-me-win.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Rectangle 886-1.png
│   │   │           │   │   ├── Rectangle 886@2x-1.png
│   │   │           │   │   └── Rectangle 886@3x-1.png
│   │   │           │   ├── icon-opponent.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Rectangle 886.png
│   │   │           │   │   ├── Rectangle 886@2x.png
│   │   │           │   │   └── Rectangle 886@3x.png
│   │   │           │   └── icon-win.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       ├── Frame 1272629367.png
│   │   │           │       ├── Frame 1272629367@2x.png
│   │   │           │       └── Frame 1272629367@3x.png
│   │   │           ├── Navigation
│   │   │           │   ├── Contents.json
│   │   │           │   ├── LeftItems
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── NavigationBack.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── Vector (Stroke).png
│   │   │           │   │   │   ├── Vector (Stroke)@2x.png
│   │   │           │   │   │   └── Vector (Stroke)@3x.png
│   │   │           │   │   ├── NavigationBack24.imageset
│   │   │           │   │   │   ├── Contents.json
│   │   │           │   │   │   ├── icon-chevron-Left.png
│   │   │           │   │   │   ├── icon-chevron-Left@2x.png
│   │   │           │   │   │   └── icon-chevron-Left@3x.png
│   │   │           │   │   └── icon-close.imageset
│   │   │           │   │       ├── Contents.json
│   │   │           │   │       ├── icon-close.png
│   │   │           │   │       ├── icon-close@2x.png
│   │   │           │   │       └── icon-close@3x.png
│   │   │           │   └── RightItems
│   │   │           │       ├── AddFriend.imageset
│   │   │           │       │   ├── Contents.json
│   │   │           │       │   ├── icon-addperson.png
│   │   │           │       │   ├── icon-addperson@2x.png
│   │   │           │       │   └── icon-addperson@3x.png
│   │   │           │       └── Contents.json
│   │   │           ├── Setting
│   │   │           │   ├── Contents.json
│   │   │           │   ├── ProfileDefault.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── Ellipse 3.png
│   │   │           │   │   ├── Ellipse 3@2x.png
│   │   │           │   │   └── Ellipse 3@3x.png
│   │   │           │   ├── copy-icon.imageset
│   │   │           │   │   ├── Contents.json
│   │   │           │   │   ├── icon-copy.png
│   │   │           │   │   ├── icon-copy@2x.png
│   │   │           │   │   └── icon-copy@3x.png
│   │   │           │   └── profile-edit-icon.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       ├── Frame 3467588.png
│   │   │           │       ├── Frame 3467588@2x.png
│   │   │           │       └── Frame 3467588@3x.png
│   │   │           ├── Splash
│   │   │           │   ├── Contents.json
│   │   │           │   └── SplashLogo.imageset
│   │   │           │       ├── Contents.json
│   │   │           │       ├── Group 238.png
│   │   │           │       ├── Group 238@2x.png
│   │   │           │       └── Group 238@3x.png
│   │   │           └── Toast
│   │   │               ├── Contents.json
│   │   │               └── circle-exclamation mark.imageset
│   │   │                   ├── Contents.json
│   │   │                   ├── circle-exclamation mark.png
│   │   │                   ├── circle-exclamation mark@2x.png
│   │   │                   └── circle-exclamation mark@3x.png
│   │   ├── Sources
│   │   │   ├── Common
│   │   │   │   └── Extensions
│   │   │   │       └── Color+Extension.swift
│   │   │   ├── Dependency
│   │   │   │   └── Dependency.swift
│   │   │   ├── Enum
│   │   │   │   ├── ColorConstants.swift
│   │   │   │   ├── CommonConstants.swift
│   │   │   │   └── ImageConstants.swift
│   │   │   ├── Features
│   │   │   │   ├── AddFriend
│   │   │   │   │   ├── AddFriendFeature.swift
│   │   │   │   │   └── AddFriendView.swift
│   │   │   │   ├── AllowAccess
│   │   │   │   │   ├── AllowAccessFeature.swift
│   │   │   │   │   └── AllowAccessView.swift
│   │   │   │   ├── Common
│   │   │   │   │   ├── CommonUI
│   │   │   │   │   │   ├── AddFriendButton.swift
│   │   │   │   │   │   ├── AddFriendTextField.swift
│   │   │   │   │   │   ├── FriendInfoView.swift
│   │   │   │   │   │   ├── ImagePicker.swift
│   │   │   │   │   │   ├── SettingContentView.swift
│   │   │   │   │   │   ├── ToastView.swift
│   │   │   │   │   │   └── ToolbarView.swift
│   │   │   │   │   └── ViewModifier
│   │   │   │   │       ├── CustomAlertViewModifier.swift
│   │   │   │   │       └── ToastModifier.swift
│   │   │   │   ├── FinishGame
│   │   │   │   │   ├── FinishGameFeature.swift
│   │   │   │   │   └── FinishGameView.swift
│   │   │   │   ├── Friend
│   │   │   │   │   ├── ModalFriend
│   │   │   │   │   │   ├── ModalFriendFeature.swift
│   │   │   │   │   │   └── ModalFriendView.swift
│   │   │   │   │   └── NormalFriend
│   │   │   │   │       ├── FriendFeature.swift
│   │   │   │   │       └── FriendView.swift
│   │   │   │   ├── Game
│   │   │   │   │   ├── GameFeature.swift
│   │   │   │   │   └── GameView.swift
│   │   │   │   ├── LegalNotice
│   │   │   │   │   └── LegalNoticeView.swift
│   │   │   │   ├── Login
│   │   │   │   │   ├── LoginFeature.swift
│   │   │   │   │   ├── LoginView.swift
│   │   │   │   │   └── SignInWithAppleCoordinator.swift
│   │   │   │   ├── Main
│   │   │   │   │   ├── MainFeature.swift
│   │   │   │   │   └── MainView.swift
│   │   │   │   ├── MatchingProcess
│   │   │   │   │   ├── MatchingProcessFeature.swift
│   │   │   │   │   └── MatchingProcessView.swift
│   │   │   │   ├── MyProfile
│   │   │   │   │   ├── MyProfileFeature.swift
│   │   │   │   │   └── MyProfileView.swift
│   │   │   │   ├── NaverMap
│   │   │   │   │   └── NaverMapView.swift
│   │   │   │   ├── Setting
│   │   │   │   │   ├── SettingFeature.swift
│   │   │   │   │   └── SettingView.swift
│   │   │   │   └── Timer
│   │   │   │       └── TimerService.swift
│   │   │   ├── Presentation.swift
│   │   │   └── Router
│   │   │       └── Router.swift
│   │   └── Tests
│   │       └── Test.swift
│   └── Shared
│       ├── Derived
│       │   └── Sources
│       │       ├── TuistAssets+Shared.swift
│       │       ├── TuistBundle+Shared.swift
│       │       └── TuistFonts+Shared.swift
│       ├── Project.swift
│       ├── Resources
│       │   ├── Assets.xcassets
│       │   │   └── Contents.json
│       │   └── Font
│       │       ├── Pretendard-Black.otf
│       │       ├── Pretendard-Bold.otf
│       │       ├── Pretendard-ExtraBold.otf
│       │       ├── Pretendard-ExtraLight.otf
│       │       ├── Pretendard-Light.otf
│       │       ├── Pretendard-Medium.otf
│       │       ├── Pretendard-Regular.otf
│       │       ├── Pretendard-SemiBold.otf
│       │       └── Pretendard-Thin.otf
│       ├── Shared.xcodeproj
│       │   ├── project.pbxproj
│       │   ├── project.xcworkspace
│       │   │   └── contents.xcworkspacedata
│       │   ├── xcshareddata
│       │   │   └── xcschemes
│       │   │       └── Shared.xcscheme
│       │   └── xcuserdata
│       │       └── incross0915.xcuserdatad
│       │           └── xcschemes
│       │               └── xcschememanagement.plist
│       ├── Sources
│       │   ├── AppState
│       │   │   └── AppState.swift
│       │   ├── Extension
│       │   │   ├── Color+Extension.swift
│       │   │   ├── Double+Extension.swift
│       │   │   ├── Font+Extension.swift
│       │   │   ├── UIViewController+Extension.swift
│       │   │   └── View+Extension.swift
│       │   ├── Log
│       │   │   └── Log.swift
│       │   ├── Shared.swift
│       │   ├── Time
│       │   │   └── Time.swift
│       │   └── UserDefaults
│       │       └── UserDefaultsManager.swift
│       └── Tests
│           └── Test.swift
├── RaceOn.ipa
├── RaceOn.xcworkspace
│   ├── contents.xcworkspacedata
│   ├── xcshareddata
│   │   ├── IDEWorkspaceChecks.plist
│   │   ├── WorkspaceSettings.xcsettings
│   │   ├── swiftpm
│   │   │   ├── Package.resolved
│   │   │   └── configuration
│   │   └── xcschemes
│   │       └── RaceOn-Workspace.xcscheme
│   └── xcuserdata
│       └── incross0915.xcuserdatad
│           ├── IDEFindNavigatorScopes.plist
│           ├── UserInterfaceState.xcuserstate
│           ├── xcdebugger
│           │   └── Breakpoints_v2.xcbkptlist
│           └── xcschemes
│               └── xcschememanagement.plist
├── Scripts
│   └── SwiftLintRunScript.sh
├── Support
│   ├── Info.plist
│   └── LaunchScreen.storyboard
├── Tuist
│   ├── Config.swift
│   ├── Package.resolved
│   ├── Package.swift
│   └── ProjectDescriptionHelpers
│       └── Project+Templates.swift
├── Workspace.swift
└── fastlane
    ├── Appfile
    ├── Fastfile
    ├── Matchfile
    ├── README.md
    └── report.xml
```

<br>

## 4. 역할 분담

### 🍊 신승욱

- **UI**
    - 페이지 : Splash, 설정, 친구, 친구 추가, 친구 선택, 경쟁 대기, 경쟁, 경쟁 종료
    - 공통 컴포넌트 : TextField, Button, ImagePicker, View, ToastView, ToolbarView
    - 기타, 그 외: Commit과 Code Review 컨벤션 정의, 일정 산정, 기획 및 디자인과 소통, Clean Architecture Boiler Plate 구축, 네이버 맵 setting
- **기능**
    - Tuist 설정
    - 네이버 맵을 활용한 기능 구현 A-Z
    - FCM Push Notification 초기 설정부터 A-Z
    - Push Notification의 데이터를 활용한 화면 이동
    - 앱 정보, 현재 버전을 나타냄
    - 경쟁 초대 알림(System Push 허용 / 비허용)제어
    - 이용약관 및 개인정보처리방침 화면으로 이동
    - 로그아웃, 회원탈퇴 구현
    - 내 프로필, 닉네임 프로필 사진 변경
    - 프로필 사진 변경시 라이브러리를 이용해 이미지를 원 모양으로 크롭
    - 내 프로필, 내 친구 코드를 복사할 수 있는 기능 구현
    - 친구 목록 보여주기(닉네임 및 프로필 이미지)
    - 신고하기, 친구 끊기 구현
    - 친구 추가 구현(친구 코드 입력)
    - 경쟁할 친구 선택(modal)
    - STOMP를 활용한 서버와 실시간 통신

<br>
    
### 👻 정진우

- **UI**
    - 페이지 : 홈, 권한 동의
    - 공통 컴포넌트 : N/A
- **기능**
    - Tuist 설정, 이외 버그

<br>

## 5. 개발 기간 및 작업 관리

### 개발 기간

- 전체 개발 기간 : 2024-11-22 ~ 2025-03-20
- UI 구현 : 2024-12-05 ~ 2025-12-16
- 기능 구현 : 2024-11-22 ~ 2025-03-12

<br>

### 작업 관리

- GitHub Projects와 Issues를 사용하여 진행 상황을 공유했습니다.
- 주간회의를 진행하며 작업 순서와 방향성에 대한 고민을 나누고 GitHub Wiki에 회의 내용을 기록했습니다.

<br>

## 6. 신경 쓴 부분

- [1]()

- [2]()

<br>

## 7. 페이지별 기능

### [초기 화면]
- 서비스 접속 초기화면으로 splash 화면이 잠시 나온 뒤 다음 페이지가 나타납니다.
    - 로그인이 되어 있지 않은 경우 : SNS 로그인 화면
    - 로그인이 되어 있는 경우 : RaceOn 홈 화면

| 초기 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [권한 화면]
- 앱 첫 설치 > 로그인, 이후 화면으로 위치 권한에 대하여 동의를 받는 화면

| 권한 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [홈 화면]
- RaceOn의 홈 화면으로 아래와 같은 기능을 제공
  - 뛸 거리 설정
  - 경쟁할 친구 선택
  - 친구 추가 및 친구 리스트 화면으로 이동
  - 설정 화면으로 이동

| 홈 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [설정 화면]
- RaceOn의 설정 화면으로 아래와 같은 기능을 제공
  - 내 프로필 화면으로 Navigation Push
  - 경쟁 초대 알림
    - RaceOn의 시스템 Push Notification 허용 / 비허용을 나타냄, Switch Touch Event시에 RaceOn 설정 화면으로 이동
  - 앱 정보, 현재 앱 버전을 나타냄
  - 이용 약관 및 개인정보처리방침
    - 터치 시 이용약관 및 개인정보처리방침 화면으로 이동(WebView)

| 설정 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [내 프로필 화면]
- RaceOn의 내 프로필 화면
  - 편집을 ON/OFF하는 toggle로 기능이 활성화
  - 닉네임 변경을 구현
  - 프로필 사진 변경 구현
    - 라이브러리를 이용하여 원모양으로 crop하는 기능 구현
  - 친구 코드를 복사하는 기능 구현 

| 내 프로필 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [친구 화면]
- RaceOn의 친구 List 화면
  - 친구 닉네임 및 프로필 사진 조회 가능
  - 친구 끊기, 친구 신고 기능 제공
  - 친구 추가 화면으로 이동하는 기능 제공
  

| 친구 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [친구 추가 화면]
- RaceOn의 친구 추가 화면
  - 해당 화면에 진입 할때 6글자의 Text가 클립보드에 저장되 있을 경우 바로 붙여넣기 기능이 제공
  - TextField를 6개로 쪼개서 하나의 TextField처럼 보이게 구현
  - 한글자 쓰면 다음 TextField로 포커스가 변경됨
  - TextField가 비어있는 상태에서 글씨를 지우면 바로 직전 TextField가 지워짐
  - 유효성 검사로 인해 6글자가 다 채워진 Case만 [친구 추가 버튼]이 활성화
  - [친구 추가 버튼]을 눌러 서버와 통신 후 친구 추가가 완료 되면 친구 List로 Navigation Pop
  

| 친구 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [친구 선택 화면]
- 홈화면에서 [경쟁할 친구 선택하기]를 터치하면 modal형태로 친구 list가 노출되고, 버튼을 누를때 서버와 통신해 친구 한명이라도 있을 경우에 노출되고 한명도 없는 경우에는 `경쟁할 친구가 없어요`라고 Toast가 노출됨.
- 친구를 선택하여(복수 선택 안됨) 경쟁할 친구를 고름
- 친구를 고르지 않으면 `[경쟁 요청하기]`버튼이 활성화 되지 않음
- 친구를 고르면 `[경쟁 요청하기]`버튼이 활성화 되고 웹소켓 `conect`를 요청함.

| 친구 선택 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [경쟁 대기 화면]
- RaceOn의 웹소켓 상태는 `Connect`, `SUBSCRIBE`, `SEND`로 나누어짐 웹소켓 상태에 따라 배경 이미지 및 Title, Subtitle가 변경됨
  - 자세한 내용은 [소켓 통신 설명](#7-1-소켓-통신-설명)에서 다루었으니 참고 바람.
- WebSocket의 경쟁할 인원 두명이 `Connect -> SUBSCRIBE -> SEND` 했다면 3초뒤에 [경쟁 화면](#경쟁-화면)으로 이동.

| 경쟁 대기 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [경쟁 화면]
- 해당 화면의 기능은 아래와 같습니다.
  - 경쟁 거리는 3/5/10km로 나누어지고 두 경쟁자는 일정 시간 마다(3초) WebSocket에 데이터를 전송
  - 내가 뛴거리, 상대가 뛴거리를 상단에 표시
  - 실시간으로 내가 뛴거리/상대 뛴거리를 확인 할 수 있음
  - 내가 뛴거리/상대가 뛴거리를 비교해 그라데이션 배경색 변경
  - 내가 뛰어온 거리 MapView에 표시
  - 내 페이스, 뛴 거리, 뛴 시간 표시
  - 게임 종료(WebSocket Disconnect) 기능 제공
  
| 경쟁 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

### [경쟁 종료 화면]
- 경쟁이 종료되는 시점의 화면
- 내 프로필 이미지가 노출되며, **승/패 여부에 따라 배경 Color**도 변경됨.
- 내가 뛴거리, 평균 페이스를 화면에 노출하고 내가 뛰어온 거리를 MapView에 동선 표시.
- 상대방의 프로필 이미지, 닉네임, 뛰어온 거리도 화면에 노출
  
| 경쟁 종료 화면 |
|----------|
|![splash](https://user-images.githubusercontent.com/112460466/210172920-aef402ed-5aef-4d4a-94b9-2b7147fd8389.gif)|

<br>

## 7-1. 소켓 통신 설명
- [소켓 통신 설명](https://docs.runner-dev.shop/#_프로토콜_설명)

<br>

## 8. 트러블 슈팅

- [1]()

- [2]()

<br>

## 9. 개선 목표

- API 모듈화 : API를 불러오는 코드의 반복이 많아 모듈화할 예정
- lighthouse Performance 증진
    - 모든 페이지에서 특히 Best Practices & SEO 점수는 90~100으로 우수
    - Performance 점수가 대체적으로 미흡한 문제
    
    ![KakaoTalk_Photo_2023-01-04-16-55-30](https://user-images.githubusercontent.com/112460466/210591134-09bf8efd-3c34-4b99-a3d7-895ca99e1457.png)
    
- **23-01-17 성능 개선 내용**
    
    ![성능개선 후](https://user-images.githubusercontent.com/106502312/212872369-7ceeb2cf-d551-41d2-bfb0-01e35e9903fe.png)
    
    - 이미지 최적화
        - `<img>` 요소에 `width` , `height` 속성값을 명시해 불필요한 Reflow를 방지했습니다.
        - browser-image-compression 라이브러리를 사용해 유저가 업로드하는 이미지를 압축했습니다.
        - Intersection Observer API를 사용해 Lazy Loading 기법을 적용하여 홈 피드의 게시글 이미지가 viewport 내에 들어오는 순간 로딩되도록 변경했습니다.
    - 웹폰트 최적화
        - WOFF2 포맷을 추가하고 가장 우선적으로 적용되도록 선언했습니다.
        - 서브셋 폰트로 교체해 용량을 줄였습니다.
    
<br>

## 10. 프로젝트 후기

### 🍊 신승욱

이번 프로젝트를 통해 여러 가지 새로운 기술을 배울 수 있어서 뜻깊은 경험이었습니다. 특히 Tuist와 TCA를 처음 사용해 본 것이 가장 인상적이었습니다.

iOS 개발을 할 때 협업 중 .xcodeproj의 충돌 문제는 흔한 일이었는데, Tuist를 사용하면서 이 문제를 완벽하게 해결할 수 있었습니다. 물론 러닝 커브가 다소 있는 점이 아쉬웠지만, 이를 극복한 이후에는 협업이 훨씬 수월해졌습니다.

또한, TCA를 적용해보면서 기존에 사용하던 ReactorKit과의 유사성을 발견할 수 있었고, 덕분에 비교적 빠르게 적응할 수 있었습니다. TCA의 강력한 상태 관리 방식과 사이드 이펙트 처리는 유지보수성을 크게 향상시키는 데 도움을 주었습니다. 다만, 액션과 상태를 엄격하게 정의해야 하는 점에서 처음에는 약간 부담스럽기도 했지만, 프로젝트가 커질수록 이러한 구조가 코드의 일관성을 유지하는 데 매우 유용하다는 것을 실감했습니다.

이번 프로젝트를 통해 클린 아키텍처의 중요성도 다시 한번 체감할 수 있었습니다. 모듈화된 구조 덕분에 도메인 로직이 UI와 분리되어 유지보수성과 확장성이 훨씬 좋아졌습니다. 앞으로도 이러한 설계를 더 적극적으로 활용해볼 계획입니다!

<br>

### 정진우

N/A

<br>
