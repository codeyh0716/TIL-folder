# 0716
## GUI/CLI
**GUI** (Graphic User Interface)

그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식

**CLI** (Command Line Interface)

명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식

## 문법 및 활용
**.** : 현재 디렉토리

**..** : 현재의 상위 디렉토리 (부모폴더)

**touch**: 파일 생성

**mkdir**(make directory): 새 디렉토리 생성

**ls**(list): 현재 작업 중인 디렉토리 내부의 폴더/파일 목록을 출력

**cd**: 현재 작업 중인 디렉토리를 변경(위치 이동)

**start**: 폴더/파일을 열기

**rm**(remove): 파일 삭제(디렉토리 삭제는 -r 옵션을 추가 사용)

**pwd**: 현재 작업 중인 폴더(디렉토리)의 절대 경로를 출력

## 경로
**루트 디렉토리**(/): 모든 주소의 시작점
**홈 디렉토리**(~): 터미널을 처음 켰을 때 시작하는 나의 기본 공간

## Markdown
(#): 제목

(1. 2. 3.): 리스트

``` python 
('hello')
```

[google](https://www.google.com/)

![이미지](https:/picsum.photos/200/300)

(**): 굵게

(*): 기울임

(~~ ~~): 취소선

(---): 수평선

## Git
### git의 영역

- **Working Directory** 실제 작업 중인 파일들이 위치하는 영역
- **Staging Area** Working Directory에서 변경된 파일 중, 다음 버전에 포함시킬 파일들을 선택적으로 추가하거나 제외할 수 있는 중간 준비 영역
- **Repository** 버전 이력과 파일들이 영구적으로 저장되는 영역. 모든 버전과 변경 이력이 기록됨

*Commit(버전): 변경된 파일들을 저장하는 행위*

---
## git의 동작
- **git init**: 로컬 저장소 설정(초기화)
- **git add**: 변경사항이 있는 파일을 staging area에 추가
- **git commit**: staging area에 있는 파일들을 저장소에 기록
---
## git 기타 명령어
- **git status**: 현재 로컬 저장소의 파일 상태 보기
- **git log**: commit history 보기
- **git log --oneline**: commit 목록 한 줄로 보기
- **git config --global -l**: git global 설정 정보 보기
---
### git commit 실습
1. 바탕화면에 git_commit 폴더를 만들고 git 저장소 생성
   
        cd ~
   
        cd Desktop
   
        mkdir git_commit
   
        cd git_commit
   
        git init 
2. 해당 폴더 안에 a.txt라는 텍스트 파일을 만들고, "add a.txt"라는 커밋 메세지로 커밋 생성

        touch a.txt
        git add a.txt
        git commit -m "add a.txt"
3. 이번에는 b.txt라는 텍스트 파일을 만들고, "add b.txt"라는 커밋 메세지로 커밋 생성

        touch b.txt
        git add b.txt
        git commit -m "add b.txt"
4. a.txt 파일을 수정하고, "update a.txt"라는 커밋 메세지로 커밋 생성

        start a.txt
        텍스트파일에 타이핑 후 컨트롤 + s 로 저장
        git add a.txt
        git commit -m "update a.txt"
        git status
        git log
## commit 수정하기
**git commit --amend**

0. 사전준비
    1. git-amend-practice 폴더 생성
   
        ```mkdir git-amend-practice```
    2. 생성한 폴더로 이동
        
        ```cd git-amend-practice```
    3. VSCode 실행

        ```code .```
    4. Git 저장소 생성

        ```git init```
1. Commit 전체 수정
    
# 0717