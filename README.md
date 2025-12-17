# Today I learned
- 2025_12_17 (수)요일에 학습한 Git/ Github 관련 내용을 기록
  
## Git 초기 설정
1. 누가 커밋 기록을 남겼는지 확인할 수 있도록 Username과 Email을 설정한다. 
   - git config --global user.name "SeungHoHwang"
   - git config --global user.email "seunghohwang734@gmail.com"
   - git config --global init.defaultBranch main
  
2. Git은 Working Directory -> Staging Area -> Repository 의 과정으로 버전 관리를 수행합니다.

## Git 기본 명령어
### 1. 현재 작업 중인 디렉토리를 Git으로 관리한다는 명령어 기입합니다.
   - git init
   - `.git`이라는 숨김 폴더를 생성하고, 터미널에는 `(main)`라고 표기됩니다. 
- `주의 사항 `  
    1. 터미널에 이미 Main이 있다면, git init을 절대 입력하면 안됩니다.
    2. 절대로 홈 디렉토리에서 git init을 하지않습니다. 터미널의 경로가 `~`인지 확인합니다.
   
### 2. git status
- Working Directory Staging Area에 있는 파일의 현재 상태를 알려주는 명령어
- 어떤 작업을 시행하기 전에 수시로 status 확인하면 좋습니다.
    1. `Untracked` : Git이 관리하지 않는 파일
    2. `Tracked` : Git이 관리하는 파일
       1. `Unmodified` : 최신 상태
       2. `Modified` : 수정되었지만 아직 Staging Area에는 반영되지 않은 상태
       3. `Staged` : Staging Area에 올라간 상태

### 3. git add
  - Working Directory에 있는 파일을 Staging Area로 올리는 명령어
  - Git이 해당 파일을 추적(관리)할 수 있도록 만듭니다.
  - `Untracked, Modified -> Staged` 상태로 변경합니다.

### 4. git commit
  - Staging Area에 올라온 파일을 하나의 버전 (커밋)으로 저장합니다. 
  - `git commit -m ""`
  - 대괄호 사이에 커밋 메시지를 넣어 줍니다.

### 5. git log
  - 커밋의 내역 `ID, 작성자, 시간, 메세지 등`을 조회할 수 있는 명령어
  - 옵션 
    - --oneline : 한 줄로 축약해서 보여줍니다.