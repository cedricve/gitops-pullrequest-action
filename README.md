# GitOps action for updating a GitOps repository through a pull request

This action allows to create a pull request on a remote GitOps repository. 

Example usage:

```yaml
steps:
- name: Create GitOps Pull Request
  uses: cedricve/gitops-pullrequest-action@master
  with:
    ssh-key: ${{ secrets.SECRET_WITH_SSH_KEY }}
    gitops-repo: "uug-ai/gitops"
    gitops-pr-branch: "release-hub-frontend-v1.0.1"
    gitops-file: "environments/staging/kerberos-hub/values.yaml"
    gitops-key: "kerberoshub.frontend.tag"
    gitops-value: "v1.0.1"
    commit-email: "gitops@uug.ai"
    commit-name: "GitOps"
    commit-mesage: "A new release for Kerberos Hub v1.0.1"
```
