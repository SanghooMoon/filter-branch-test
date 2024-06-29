# filter-branch-test
fileter-branch(커밋이력 지우기) 기능 테스트를 위한 저장소

시나리오
1. 깃 연결 후 프로젝트를 세팅하여 개발(커밋)을 진행합니다.
2. 개발을 진행하면서 커밋이 쌓입니다.
3. 실수로 인해 민감한 정보인 key이 담긴 파일을 github에 올려버립니다.
4. 해당 파일을 삭제하고 커밋했지만, 커밋 이력을 확인하면 해당 정보를 볼 수 있습니다.
5. 위 문제를 해결하기 위해 해당 파일과 관련된 커밋 이력을 삭제하는 작업을 진행합니다.

작업을 진행한다고 가정하기 위한 샘플 커밋
계속 작업 진행중!!

git filter-branch -f --index-filter "git rm --cached --ignore-unmatch ./src/key.txt" --prune-empty -- --all