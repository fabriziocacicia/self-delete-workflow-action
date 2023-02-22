# Self Delete Workflow Action
An action that deletes the workflow that launches it. It is a self-destruction operation, once run the workflow will be gone.

**WARNING!!**

It deletes the folder where the workflow is defined and commit the changes to the repository. The changes will be final and cannot be reverted once completed.


The action is able to make changes on protected branches. It push the changes to a temporary branch and then merge them with a Pull Request.

## Usage
Add the action in your worklow as follows. You have to pass a Personal Access Token with the proper permissions to edit repositories and create and delete pull requests.

```yaml
- name: Self Delete Workflow
  uses: fabriziocacicia/self-delete-workflow-action@v0.1.0
    env:
      GITHUB_TOKEN: ${{ secrets.PERSONAL_ACCESS_TOKEN }}
```
