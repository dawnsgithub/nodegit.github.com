---
layout: default
menu_item: api
title: Revert
description: Version 0.19.0
menu_item: api
return_to:
  "API Documentation Index": /api/
sections:
  "commit": "#commit"
  "revert": "#revert"
---

## <a name="commit"></a><span>Revert.</span>commit <span class="tags"><span class="async">Async</span></span>

```js
Revert.commit(repo, revert_commit, our_commit, mainline, merge_options).then(function(index) {
  // Use index
});
```

Reverts the given commit against the given "our" commit, producing an index
that reflects the result of the revert.

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | the repository that contains the given commits. |
| revert_commit | [Commit](/api/commit/) | the commit to revert |
| our_commit | [Commit](/api/commit/) | the commit to revert against (e.g. HEAD) |
| mainline | Number | the parent of the revert commit, if it is a merge |
| merge_options | [MergeOptions](/api/merge_options/) | the merge options (or null for defaults) |

| Returns |  |
| --- | --- |
| [Index](/api/index/) | the index result |

## <a name="revert"></a><span>Revert.</span>revert <span class="tags"><span class="async">Async</span></span>

```js
Revert.revert(repo, commit, given_opts).then(function(result) {
  // Use result
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | the repository to revert |
| commit | [Commit](/api/commit/) | the commit to revert |
| given_opts | [RevertOptions](/api/revert_options/) | the revert options (or null for defaults) |

| Returns |  |
| --- | --- |
| Number |  zero on success, -1 on failure. |

