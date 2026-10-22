# jbeat-plugins

Jbeat 플러그인을 Claude Code에 등록하는 마켓플레이스 목록 저장소
플러그인 본체는 각 저장소에 있고, 이 저장소는 목록(`.claude-plugin/marketplace.json`)과 고정 버전(`ref`)만 관리

## 등록

```
/plugin marketplace add jbeat30/jbeat-plugins
```

## 플러그인

| 플러그인 | 설치 | 저장소 |
| --- | --- | --- |
| jbeat-conventions | `/plugin install jbeat-conventions@jbeat-plugins` | [jbeat30/jbeat-conventions](https://github.com/jbeat30/jbeat-conventions) |
| agent-team-base | `/plugin install agent-team-base@jbeat-plugins` | [jbeat30/agent-team-base](https://github.com/jbeat30/agent-team-base) |

두 플러그인은 서로 독립이며 하나만 설치해도 됨

## 버전

- 각 플러그인 항목의 `ref`가 배포 버전(태그)
- 플러그인 릴리즈 후 소유자가 main의 `.claude-plugin/marketplace.json`에서 `ref`만 수정해 직접 커밋
- 사용자는 `/plugin marketplace update jbeat-plugins` 실행 시 반영
- 소유자 외 쓰기 불가, 이슈·위키·프로젝트·Actions 비활성

## 기존 `jbeat30/jbeat-conventions`로 등록한 환경

```
/plugin marketplace remove jbeat-plugins
/plugin marketplace add jbeat30/jbeat-plugins
```
