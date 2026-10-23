# 프로필 적용 안내

현재 패키지는 **게시되지 않은 로컬 초안**입니다. 저장소 생성·push·Actions 실행은 하지 않았습니다.

## 승인 후 적용

1. 공개 게시를 승인한 뒤 `jihyungkim0011/jihyungkim0011` 공개 저장소를 만들거나 기존 저장소에 적용합니다. 기존 파일은 먼저 백업하고 충돌을 확인하세요.
2. `README.md`뿐 아니라 `profile/`, `profile-3d-contrib/`, **숨김 폴더 `.github/`**까지 복사합니다. `SETUP.md`는 운영 설명용으로 함께 보관해도 됩니다.
3. GitHub Actions 사용이 허용되어 있는지 확인합니다. 조직·계정 정책이 차단하면 관리자에게 확인하세요. 별도 PAT/시크릿이나 Gist는 필요 없습니다.
4. 기본 브랜치에 workflow가 반영된 뒤 **Actions → Update profile visuals → Run workflow**를 실행합니다. 이 실행은 두 SVG를 저장소에 커밋합니다. 기본 브랜치 보호 규칙이 봇 push를 막으면 정책을 우회하지 말고 허용된 배포 절차를 확인하세요.
5. 성공 후 README와 두 이미지가 교체되는지 확인합니다. 첫 실행 전 이미지는 실제 통계가 아닌 **명시적인 생성 대기 안내**입니다.

매일 UTC 19:37 / 한국시간 04:37에 갱신합니다. GitHub 스케줄은 지연될 수 있고, 공개 저장소가 60일 동안 활동이 없으면 예약 실행이 비활성화될 수 있습니다. 필요하면 Actions에서 다시 활성화하세요.

## 무엇을 표시하나요?

- 통계 카드: 공개 GitHub 활동. `include_all_commits=false`이므로 Total Commits는 올해 기준입니다. 별·PR·이슈 등의 집계 범위는 제공 액션의 정의를 따릅니다. 모든 지표를 같은 기간의 숫자로 해석하지 마세요.
- 3D 달력: 기본값인 최근 약 1년의 GitHub 기여 달력입니다. **기여 수 ≠ 커밋 수**입니다. PR·이슈 등도 기여에 포함될 수 있고, 커밋 인정에는 GitHub의 계정·브랜치 등 조건이 적용됩니다.
- 공개 정보에 접근하는 내장 `github.token`만 사용합니다. 비공개 저장소 정보 접근을 위한 PAT를 추가하지 않습니다. 계정이 익명 비공개 기여 수를 공개하도록 설정했다면 공개 달력에 그 수가 포함될 수 있습니다.
- 프로젝트 설명과 기술은 확인된 각 저장소 README를 기반으로 했습니다. 개인 기여 범위나 성능 개선 수치는 주장하지 않았습니다. 이력서 원문 링크와 연락처는 포함하지 않았습니다.

## 안전 장치와 한계

- 실행 저장소를 `jihyungkim0011/jihyungkim0011`로 제한했습니다.
- 권한은 해당 저장소의 `contents: write`만 명시합니다. 액션은 커밋 SHA로 고정했습니다. 액션 내부 패키지·런타임 의존성 전체가 고정되었다는 뜻은 아닙니다.
- 두 생성 단계와 SVG 검증이 모두 성공해야 커밋합니다. 실패하면 원격 저장소의 기존 이미지가 유지됩니다. 다른 파일은 커밋하지 않습니다.
- 동시 실행을 직렬화합니다. 사용자가 같은 시점에 push하여 충돌하면 강제 push 없이 실패하므로 최신 상태에서 다시 실행하세요.
- 로컬에서는 XML, 상대 경로와 YAML 구조를 검증했습니다. 브라우저 렌더는 환경의 소켓 제한으로 실행하지 못해 GitHub 전체 레이아웃·모바일 화면은 미검증입니다. 실제 GitHub Actions 실행·권한·API 결과는 **미검증**입니다.
- 기술 배지는 Shields.io 외부 이미지입니다. 통계와 3D 이미지는 저장소 내부 파일입니다. 장식용 헤더·프로젝트 이미지와 애니메이션은 사용하지 않습니다.

## 참고

- [Stats Action 입력 명세](https://github.com/stats-organization/github-readme-stats-action/blob/2c498845f71017821efaad14293ebc736156ef21/action.yml)
- [3D 기여 달력 사용법](https://github.com/yoshi389111/github-profile-3d-contrib/tree/7d95e7d4cdc028dd1e1cbd957d65f35efb12ae39)
- [GitHub 프로필 README](https://docs.github.com/en/account-and-profile/how-tos/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)

ZIP에는 README·통계 및 3D 이미지·workflow·이 안내만 포함합니다. 이전 장식형 아트워크 미리보기는 이 심플 버전에 해당하지 않습니다.
