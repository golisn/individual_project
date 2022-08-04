# individual_project

conda env create -f ex.yaml
  오류시 확인사항
    conda update -n base conda


git clone '연동할 git링크 ex)https://github.com/golisn/individual_project.git'

연동하여 생긴 폴더로 진입
  cd 폴더명
  
django-admin startproject dj .(.은 현재 폴더 경로로 생성한다는 뜻)

git 토큰 생성
  settings -> developer settings -> personal acces tokens -> generate new token -> 권한부여(연동에는 repo권한필요)
  -> generate token

python manage.py mkmigrations 는 변동된 사항을 임시추출하는 명령
python manage.py migrate 는 임시추출한 내용을 저장한다.
python manage.py createsuperuser(사용할 수퍼계정생성)

git config -global useremail'git이메일주소입력'
git config -global username'gitname입력'
git commit -m '지금 commit할 프로젝트 이름'
git add . (.은 모든 파일을 의미함 특정 파일만 올릴수 있음)
git push
  user name: 'gitname 입력'
  password: '생성한 토큰입력'
  
git 연동 오류시 확인사항
  제어판 -> 자격증명관리자 -> windows자격증명 ->  git:http://github.com 제거 -> 일반 자격 증명 추가 
  -> 네트워크 주소 git:http://github.com 재등록
