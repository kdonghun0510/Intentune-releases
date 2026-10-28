# Intentune

Intentune은 macOS에 설치·로그인된 Claude Code·Codex CLI를 구독 그대로 써서, 요청의 의도를 요구사항과 결정으로 정리하고 실행·검증·복구까지 이어 주는 로컬 개발 데스크톱 앱입니다. API 키를 쓰지 않습니다.

📄 [Intentune 소개서 (PDF)](https://github.com/kdonghun0510/Intentune-releases/blob/main/docs/Intentune-overview-ko.pdf) · [English](https://github.com/kdonghun0510/Intentune-releases/blob/main/docs/Intentune-overview-en.pdf)

Intentune is a local desktop app for development on macOS. It runs the Claude Code and Codex CLIs you have installed and signed in to — on your subscription, with no API keys — and takes a request from its intent to requirements and decisions, then through running, checking and recovery.

📄 [Intentune overview (PDF)](https://github.com/kdonghun0510/Intentune-releases/blob/main/docs/Intentune-overview-en.pdf) · [한국어](https://github.com/kdonghun0510/Intentune-releases/blob/main/docs/Intentune-overview-ko.pdf)

**최신 버전 / Latest release: [releases/latest](https://github.com/kdonghun0510/Intentune-releases/releases/latest)** · [모든 릴리스 / All releases](https://github.com/kdonghun0510/Intentune-releases/releases)

- [설치 (한국어)](#설치)
- [Install (English)](#install)
- [문의·신고 / Help & feedback](#문의신고--help--feedback)

## 설치

> Intentune은 Apple Developer ID로 서명·공증되지 않은 ad-hoc 서명 앱입니다. 처음 한 번은 macOS가 실행을 막으며, 아래 4단계처럼 시스템 설정에서 직접 허용해야 합니다(터미널 명령 불필요).

요구 사항: macOS 13 이상의 Apple Silicon Mac, 구독으로 로그인한 Claude Code 또는 Codex CLI. 의미 검색은 macOS 14 이상에서 켜집니다.

1. [최신 릴리스](https://github.com/kdonghun0510/Intentune-releases/releases/latest)에서 `Intentune-<version>-arm64.dmg`를 내려받습니다.
2. DMG를 열고 **Intentune**을 **Applications** 폴더로 드래그합니다. DMG 안에서 바로 실행하지 마세요 — macOS가 임시 격리 위치에서 실행해 앱 내 업데이트가 동작하지 않습니다.
3. 응용 프로그램 폴더에서 Intentune을 엽니다. **"Apple은 'Intentune'에 악성 코드가 없음을 확인할 수 없습니다"** 경고가 뜨면 **완료**를 누릅니다(**휴지통으로 이동은 누르지 마세요**).
4. **시스템 설정 › 개인정보 보호 및 보안**을 열고 아래쪽 *"Intentune"이(가) 차단되었습니다* 옆의 **그래도 열기**를 누른 뒤, 암호/Touch ID로 확인하고 다시 **그래도 열기**를 누릅니다.
5. 이후에는 평소처럼 실행되며, 앱 내 업데이트도 이 경고 없이 설치됩니다.

### "손상되었기 때문에 열 수 없습니다"가 뜰 때

"손상되었기 때문에 열 수 없습니다"(그래도 열기 없음)가 뜨면 위와 다른 문제(다운로드·서명 손상)입니다. DMG를 다시 받거나 [버그 신고](https://github.com/kdonghun0510/Intentune-releases/issues/new?template=bug.yml)로 알려 주세요. 임시 우회: DMG 안의 `Fix damaged.command`를 실행합니다(`xattr -cr /Applications/Intentune.app` 한 줄). 정식 설치 과정은 아닙니다.

## Install

> Intentune is ad-hoc signed; it is not signed or notarized with an Apple Developer ID. The first time, macOS blocks it, and you allow it yourself in System Settings as in step 4 below (no Terminal commands needed).

Requirements: an Apple Silicon Mac with macOS 13 or later, and Claude Code or the Codex CLI signed in with a subscription. Semantic search needs macOS 14 or later.

1. Download `Intentune-<version>-arm64.dmg` from the [latest release](https://github.com/kdonghun0510/Intentune-releases/releases/latest).
2. Open the DMG and drag **Intentune** to the **Applications** folder. Do not run it from inside the DMG — macOS would run it from a temporary quarantined location, and in-app updates would not work.
3. Open Intentune from Applications. If you see **"Apple could not verify 'Intentune' is free of malware"**, press **Done** (**do not press Move to Trash**).
4. Open **System Settings › Privacy & Security**, press **Open Anyway** next to *"Intentune" was blocked* near the bottom, confirm with your password or Touch ID, and press **Open Anyway** again.
5. From then on it opens normally, and in-app updates install without this warning.

### "Intentune is damaged and can't be opened"

If macOS says the app **is damaged and can't be opened** (with no Open Anyway), that is a different problem: the download or its signature is broken. Download the DMG again, or tell us with a [bug report](https://github.com/kdonghun0510/Intentune-releases/issues/new?template=bug.yml). As a temporary workaround, run `Fix damaged.command` from the DMG (one line: `xattr -cr /Applications/Intentune.app`). It is not part of the normal install.

## 문의·신고 / Help & feedback

Intentune은 개인이 운영하며 응답이 늦을 수 있습니다. / Intentune is run by one person, so replies may take a while.

| | 어디로 / Where |
|---|---|
| 버그 / Bugs | [Issues — 버그 신고 / Bug report](https://github.com/kdonghun0510/Intentune-releases/issues/new?template=bug.yml) |
| 질문 / Questions | [Discussions — Q&A](https://github.com/kdonghun0510/Intentune-releases/discussions/categories/q-a) |
| 기능 제안 / Ideas | [Discussions — Ideas](https://github.com/kdonghun0510/Intentune-releases/discussions/categories/ideas) |
| 보안 문제 / Security | [SECURITY.md](SECURITY.md) — 공개 글로 올리지 마세요 / do not post publicly |

앱에서도 **Preferences › 문의·신고**나 도움말 패널의 [문제 신고]·[질문·제안]으로 바로 갈 수 있습니다. [진단 정보 복사]는 앱·macOS 버전, CLI 상태, 최근 오류 코드를 경로와 토큰을 뺀 채 클립보드에 복사합니다.

In the app, **Preferences › Help & feedback** and the help panel have [Report a problem] and [Questions & ideas]. [Copy diagnostics] copies the app and macOS versions, the CLI state and recent error codes to the clipboard, without paths or tokens.
