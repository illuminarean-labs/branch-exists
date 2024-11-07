# Hello Branch Exists Action! 👋
해당 액션은 특정 Repository에 브런치가 존재하는지 체크하는 액션입니다. (타 Repository의 브런치도 활용 가능) 

# Token Permission
토큰에는 존재 확인을 원하는 Repository를 읽을 수 있는 멤버의 `repo:read` 권한이 필요합니다.

# Usage
```yaml
- name: Check branch exists in Cloud config repository
  uses: illuminrean-labs/branch-exists@v1
  id: check-branch
  with: 
    branch: 'some-branch'
    repository: 'owner/repo'
    token: ${{ secrets.GH_TOKEN }}
- name: Echo Exists
  run: echo "Exists ${{ steps.check-branch.outputs.exists }}"
```
