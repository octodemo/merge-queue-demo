# Merge Queue Demo

This project was made for demoing GitHub Merge Queue. Go run the Actions to create pull requests that will pass or fail checks in the merge queue.

## Getting Started
1. Clone this repository.
2. Push it to your own GitHub organization.
3. Create a repository secret named `USER_PAT`.
	If you use a classic PAT, give it the `repo` scope.
	If you use a fine-grained PAT, grant it access to this repository with:
	`Contents: Read and write`
	`Pull requests: Read and write`
4. Use the actions workflows to create PRs that will pass or fail checks in the merge queue, add PRs to the merge queue, and close open PRs.

`USER_PAT` is used by the PR creation workflows to push branches and create pull requests, and by the merge conflict demo workflow to merge a PR into the merge queue.

## Actions

### Open Bad PRs
Opens X number of PRs that will pass checks but fail checks in the merge queue.

### Open Good PRs
Opens X number of PRs that will pass checks and pass checks in the merge queue.

### Merge Conflict PRs
Opens 2 PRs that will pass checks but conflict with each other in the merge queue.

### Add Prs to Queue
Adds all open PRs to the merge queue.

### Close Open PRs
Closes all open PRs.

## Resources
* [Managing a merge queue](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-a-merge-queue)
* [Merging a pull request with a merge queue](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request-with-a-merge-queue)
