# 실습 아카이브 (웹에서 직접 고침)

스마트 인터랙션 디자인 수업에서 만든 실습을 모아 두는 내 웹사이트입니다.
카탈로그 92개마다 **따라 하기 1개 + 내 응용 1개**, 모두 **184개**를 이곳에 올립니다.
TA와 교수님은 이 사이트로 실습을 확인하고, 수강생끼리 서로의 작업을 볼 수 있습니다.

- 내 사이트 주소: `https://<내 GitHub 아이디>.github.io/si-archive/`
- **만들기는 Claude**, **올리기는 GitHub Desktop 앱**이 합니다. 코드와 터미널은 쓰지 않습니다.
- 이 사이트는 **인터넷에 공개**됩니다(무료 GitHub는 공개 저장소에서만 사이트를 만들 수 있어요). 전화번호·학번·주소 같은 개인 정보는 넣지 마세요. 이름 대신 별명을 써도 됩니다.

### 도구 두 개의 역할
| | 하는 일 | 비유 |
|---|---|---|
| **Claude 데스크톱 앱 · Code 탭** | 실습 파일을 만들고 고칩니다 | 작업대 |
| **GitHub Desktop** | 바뀐 것을 확인하고, 저장하고, 서버에 올립니다 | 택배 창구 |

### 처음 나오는 말 풀이
- **GitHub**: 내 파일을 인터넷에 보관해 주는 서비스(창고)입니다. **저장소(repository)** 는 그 안에 있는 내 프로젝트 폴더 하나입니다.
- **GitHub Pages**: 창고에 있는 파일을 누구나 열어 볼 수 있는 웹사이트로 보여 주는 무료 기능(전시장)입니다.
- **공개(Public)**: 주소를 아는 누구나 볼 수 있다는 뜻입니다.
- **브랜치(branch)와 `main`**: 같은 저장소 안의 작업 줄기에 붙은 이름입니다. 보통은 `main` 하나만 보입니다(수업에서 이름을 하나로 정할지는 아직 정해지지 않았어요. 다른 이름이 보이면 TA에게 알려 주세요).
- **충돌(conflict)**: 같은 곳을 두 군데에서 따로 고쳐서, 앱이 자동으로 합치지 못하겠다고 알려 주는 화면입니다. 이 화면이 뜨면 아무것도 누르지 말고 TA를 부르세요.
- **noreply 이메일**: 진짜 이메일 대신 쓰는 가짜 주소입니다. 올린 기록에 내 진짜 이메일이 남지 않게 해 줍니다.

### 꼭 알아 둘 화면 요소 (GitHub Desktop)
상단의 **Commit to main** · **Push origin** · **Fetch origin / Pull origin**(상태에 따라 글자가 바뀜), 왼쪽의 **History 탭**, 기록을 오른쪽 클릭하면 나오는 **Revert Changes in Commit**. (`main` 자리에 다른 이름이 보이면 그 이름이 현재 브랜치입니다. 버튼 역할은 같지만 TA에게 알려 주세요.)

| 버튼 | 뜻 | 언제 |
|---|---|---|
| **Commit to main** | 지금 상태를 사진 찍듯 **저장** | 실습 하나를 끝냈을 때 |
| **Push origin** | 저장한 것을 서버로 **올리기 = 제출** | Commit 바로 다음 |
| **History 탭** | 지금까지 저장한 **기록** | 언제 무엇을 저장했는지 볼 때 (저장과 올리기는 따로입니다) |
| **Revert Changes in Commit** (기록 오른쪽 클릭) | 그 기록 **전체를 취소** | 망쳤을 때 |
| **Fetch / Pull origin** | 서버의 최신 상태를 **받아 오기** | 다른 컴퓨터에서 이어 할 때 |

> 철칙 두 개: **① GitHub 웹사이트에서 파일을 직접 고치지 않기** (내 컴퓨터와 서버가 어긋나 다음 올리기가 막힙니다) · **② 공개되면 안 되는 정보 넣지 않기** (지워도 기록에 남습니다)

---

## 처음 한 번 — 준비와 연결

> 처음 한 번만 하면 됩니다. 메일 인증을 기다리는 시간과 공개 주소가 켜지는 시간(1~10분)이 있어서 오래 걸릴 수 있어요. 막히면 혼자 오래 붙잡지 말고 TA를 부르세요.

### 1. 계정과 앱 준비
1. **Claude 데스크톱 앱**을 최신 버전으로 업데이트하고 로그인합니다(Pro 이상). 왼쪽 위에 **Code** 탭이 보이면 OK.
   - 윈도우에서 Code 탭이 "Git을 설치하라"고 하면 git-scm.com 에서 Git을 설치한 뒤 앱을 다시 켭니다.
2. **GitHub 가입** (github.com → Sign up)
   - 아이디는 사이트 주소가 됩니다. **영문 소문자로 짧게** 정하세요.
   - 가입 후 받은 메일에서 **Verify email address** 를 꼭 누릅니다. 인증하지 않으면 다음 단계가 막힙니다.
   - GitHub 오른쪽 위 프로필 → Settings → Emails → **Keep my email addresses private** 와 **Block command line pushes that expose my email** 을 둘 다 켭니다.
3. **GitHub Desktop 설치** (desktop.github.com → Download) 후 실행합니다.

### 2. GitHub Desktop 로그인
1. 첫 화면에서 **Sign in to GitHub.com** → 브라우저가 열리면 GitHub Desktop 접근을 **승인**하고 앱으로 돌아옵니다(버튼 문구는 화면에 따라 조금 다를 수 있어요).
   - 비밀번호나 인증 코드는 Claude·TA·친구에게 보내지 않습니다. 직접 입력합니다.
2. Git 설정 화면이 나오면 이름은 내 GitHub 아이디, 이메일은 목록에서 **`…@users.noreply.github.com`** 으로 끝나는 주소를 고릅니다(개인 이메일이 공개되지 않게).
   - 목록에 그 주소가 없으면 **개인 이메일로 진행하지 말고** 로그아웃 후 다시 로그인, 그래도 없으면 TA를 부릅니다.
   - 지나쳤다면: GitHub Desktop 메뉴 → Settings(윈도우는 File → Options) → **Git** 에서 바꿉니다.

### 3. 내 폴더 만들기
1. 수업에서 받은 압축 파일을 **문서 폴더**에 풀고, 폴더 이름을 **`si-archive`** 로 바꿉니다.
   - 바탕화면·iCloud Drive·OneDrive 같은 자동 동기화 폴더는 피하세요.
2. GitHub Desktop → **File → Add Local Repository…** → `si-archive` 폴더 선택 (메뉴 글자는 맥·윈도우에서 조금 다르게 보일 수 있어요)
3. "이 폴더는 아직 저장소가 아니다"라는 안내가 나오면 그 안의 **저장소 만들기(create a repository)** 링크를 누릅니다. 이름이 `si-archive` 인지 확인하고, **Initialize this repository with a README 는 체크 해제**, Git Ignore·License 는 **None** 으로 둔 뒤 **Create Repository**.
4. **(화면을 보고 고르세요)** 왼쪽 **Changes** 에 파일이 보이고 왼쪽 아래 **Commit to main** 버튼이 눌리는 상태라면, 파일을 모두 체크된 그대로 두고 **Summary** 에 `처음 올리기` 라고 쓴 뒤 **Commit to main** 을 누릅니다. 이미 Commit할 파일이 없고 위쪽에 **Publish repository** 가 보이면 이 단계는 건너뛰고 다음 단계로 갑니다. 어느 쪽인지 모르겠으면 누르기 전에 TA를 부릅니다.
   - (TA 메모: 이 단계가 실제 앱에서 꼭 필요한지는 아직 확인하지 못했습니다 — 확인 필요)

### 4. 서버에 올리기 (Publish)
1. 위쪽 **Publish repository** 를 누릅니다.
2. 이름 `si-archive` 확인, **Keep this code private 체크를 반드시 해제** → **Publish Repository**.
   - 체크된 채로 올리면 무료 계정에서는 사이트가 만들어지지 않습니다.

### 5. 공개 주소 켜기 (GitHub 웹에서 한 번만)
1. GitHub Desktop → **Repository → View on GitHub**
2. 저장소 페이지 위쪽 **Settings** → 왼쪽 **Pages**
3. **Build and deployment** → Source: **Deploy from a branch**(저장소에 있는 파일로 사이트를 만든다는 뜻) → Branch: **main** 을 고르고 옆 칸은 **/(root)** (폴더 안쪽이 아니라 저장소 맨 바깥, `index.html` 이 있는 자리라는 뜻) → **Save**
   - 앞 단계 Desktop 위쪽의 현재 브랜치 이름이 `main` 이 아니면 그 이름을 고르고 TA에게 알립니다(`main` 이 아닌 경우의 실제 모습은 아직 확인하지 못했습니다 — 확인 필요).
4. 1~10분 뒤 같은 화면 위쪽에 주소가 나옵니다. 열어서 **92행 × 2열(184칸) 격자**가 보이면 성공입니다.

### 6. 이름 넣고 주소 제출
1. Claude 앱 → **Code** 탭 → 폴더 선택에서 `si-archive` 를 고릅니다.
2. Claude에게: `첫 화면에 내 이름 넣어 줘. 공개용 이름은 ○○○, GitHub 아이디는 ○○○이야.`
3. GitHub Desktop에서 **Commit to main → Push origin** (아래 "올리기"와 같음)
4. **사이트 주소를 TA에게 제출**합니다(제출하는 방법은 수업에서 TA가 알려 줍니다).

---

## 매번 하는 일

### ① Claude에게 만들기
카탈로그(갤러리)에서 그 번호의 **한 줄** 또는 **5칸 명세**를 복사해 붙입니다. 5칸 명세는 이렇게 읽습니다: **[오브젝트]** 움직이는 대상(어느 물건이 움직이나) · **[트리거]** 언제 시작하나(무엇을 하면 시작되나) · **[반응]** 무엇이 어떻게 변하나 · **[조건]** 어떤 경우에만 그러나 · **[변수]** 화면이 기억해 두는 값.
```
23번 따라 하기 추가해 줘. 넣을 문장: (복사한 문장)
```
내 응용은 원본에서 무엇을 바꿨는지 함께 말합니다.
```
23번 내 응용 만들어 줘. 넣을 문장: (내가 쓴 문장)
이름: 재생목록 시트 / 바꾼 점: 바텀 시트를 음악 재생목록으로, 높이 3단계에 뒤 화면 어두워짐 추가
```

### ② 내 컴퓨터에서 확인
Finder(윈도우는 파일 탐색기)에서 `si-archive/works/23/mine/index.html` 을 더블클릭해 직접 조작해 보고, `si-archive/index.html` 에서 23번 칸이 채워졌는지도 봅니다.

### ③ GitHub Desktop에서 올리기
1. 왼쪽 **Changes** 에 바뀐 파일이 보입니다. 보통 **실습 파일 + `data/works.js`** 2개, 이미지·영상을 넣었으면 그 파일도 함께 보입니다(**모두 체크된 채로** 올려야 공개 사이트에서도 보여요).
   - 모르는 파일, 개인 파일, 아주 큰 파일이 있으면 **체크를 풀고** Claude에게 물어봅니다.
2. 왼쪽 아래 **Summary** 에 한 줄 (예: `23번 내 응용 추가`) → **Commit to main**
3. 위쪽 **Push origin** → 공개 주소 반영에는 최대 10분이 걸릴 수 있습니다. **이것으로 제출 끝.**
- **Commit은 실습마다 따로** 합니다. 여러 실습을 한 Commit에 묶으면 나중에 하나만 되돌릴 수 없어요.
- 여러 개를 모아 올리고 싶으면: 실습마다 Commit → 마지막에 Push origin 한 번. (GitHub Pages는 시간당 약 10번 반영의 느슨한 제한이 있어요)

## 이렇게 말하면 됩니다

| 하고 싶은 것 | Claude에게 | GitHub Desktop에서 |
|---|---|---|
| 실습 추가 | "23번 따라 하기 추가해 줘" · `/add 23 follow` | — |
| 값 하나 고치기 | "23번 내 응용에서 붙는 시간만 0.35초에서 0.5초로" | — |
| 올리기 | (Claude는 안내만 함) · `/publish` | Commit to main → Push origin |
| 되돌리기 | "방금 올린 거 취소하고 싶어" · `/undo` | History → 오른쪽 클릭 → Revert Changes in Commit → Push origin |
| 점검 | "점검해 줘" · `/check` | — |

## 다른 컴퓨터에서 이어 할 때
- **처음 쓰는 컴퓨터:** GitHub Desktop 로그인 → **File → Clone Repository…** → `si-archive` → 문서 폴더에 받기. (압축 파일을 다시 풀어 새로 만들지 마세요)
- **작업 시작 전 항상:** GitHub Desktop 위쪽 **Fetch origin** → 버튼이 **Pull origin** 으로 바뀌면 누르기.
- 두 컴퓨터에서 동시에 작업하지 않습니다.

## 지켜 주세요
- **한 번에 하나만.** 여러 개를 한꺼번에 시키면 어디서 틀렸는지 찾기 어렵습니다.
- **고칠 때는 값 하나만.** "더 멋지게"보다 "튕기는 높이만 300에서 200으로"가 정확합니다.
- **기술 이름 대신 보이는 것과 숫자로 말합니다.** 카탈로그 부록 "기술 이름 대신 쓰는 말" 참고.
- 영상·이미지는 **파일 하나 20MB 이하** (수업 기준입니다. GitHub는 약 50MB부터 경고, 약 100MB부터 거부). ProtoPie 화면 녹화는 영상(mp4) 파일로 줄여서 넣습니다. `.zip`·`.psd`·`.ai`·`.pie`·`.fig` 파일은 실수로 올라가지 않게 막아 두었으니(`.gitignore`) 넣지 마세요.
- 첫 화면(`index.html`)과 `data/works.js` 는 Claude가 관리합니다. 직접 고치지 않습니다.

## 막혔을 때

| 증상 | 해 볼 것 |
|---|---|
| 공개 주소가 404 | 반영에 최대 10분. 10분 뒤 강력 새로고침, 한 시간이 지나도 안 되면 5단계(Pages)에서 고른 브랜치 이름과 /(root) 가 저장됐는지 확인 후 TA |
| 사이트에 옛 화면이 보임 | 브라우저 강력 새로고침 (맥 ⌘⇧R · 윈도우 Ctrl+Shift+R) |
| Commit 했는데 공개 사이트에 안 보임 | 위쪽 버튼이 아직 **Push origin** 이면 올리기 전입니다. 눌러 주세요. 그다음 최대 10분 기다립니다 |
| Push가 거부됨 ("rejected", "fetch first") | **Fetch origin → Pull origin** 후 다시 Push. 그래도 안 되면 TA |
| Desktop에 "conflict"(충돌: 두 수정이 겹쳐 자동으로 합칠 수 없다는 안내)가 뜸 | 아무것도 누르지 말고 TA를 부릅니다. 화면을 사진으로 찍어 두면 도움이 됩니다 |
| 다른 실습이 망가짐 | History에서 방금 기록 Revert → Push. (그 기록에 실습이 여러 개 묶였으면 혼자 하지 말고 TA) |
| Publish 했는데 사이트가 안 생김 | 저장소가 비공개(Private)인지 확인: 저장소 Settings → 맨 아래 Danger Zone → Change repository visibility 의 **Change visibility** → Public → 확인 후 **Make this repository public** |
| 이메일 인증 안내가 계속 뜸 | 가입 메일의 Verify email address 를 누릅니다 |

## 폴더 구조
```
index.html            첫 화면 (92행 × 2열, 184칸)
data/works.js         목록 데이터 (Claude가 관리)
assets/bar.js         실습 페이지 구석 표시
works/23/follow/      23번 따라 하기
works/23/mine/        23번 내 응용
CLAUDE.md             Claude가 지킬 규칙
.gitignore            올리면 안 되는 파일 목록
.claude/commands/     단축어
```
