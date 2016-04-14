# test-squash

Testing the new github squash-from-web-ui PR functionality.

Let's say you have the following changes in your feature branch:
```
* commit 645708acdd3e6822c68995662ab2f8686307add2
| Author: jden <jden@zendesk.com>
| Date:   Thu Apr 14 14:28:30 2016 -0700
|
|     add punctuation
|
* commit 72a1153b1d0f18bc5ca70d9df0176084473e9f42
| Author: jden <jden@zendesk.com>
| Date:   Thu Apr 14 14:28:20 2016 -0700
|
|     capitalize
|
```

Previously, the PR Merge button would result in a `git log` history that looks like:
```
*   commit bb03592af7daadd345698eb8be32ccd349571f09
|\  Merge: 708589e 645708a
| | Author: jden <jden@zendesk.com>
| | Date:   Thu Apr 14 14:39:18 2016 -0700
| |
| |     Merge pull request #2 from pr
| |
| |     add punctuation
| |
| |     capitalize
| |
| * commit 645708acdd3e6822c68995662ab2f8686307add2
| | Author: jden <jden@zendesk.com>
| | Date:   Thu Apr 14 14:28:30 2016 -0700
| |
| |     add punctuation
| |
| * commit 72a1153b1d0f18bc5ca70d9df0176084473e9f42
|/  Author: jden <jden@zendesk.com>
|   Date:   Thu Apr 14 14:28:20 2016 -0700
|
|       capitalize
|
```

With the squash and merge button, it results in:

```
* commit 3539f9a6ff46a15067e264be0ee0ca99d903aa48
| Author: Jason Denizac <jason@denizac.org>
| Date:   Thu Apr 14 14:34:52 2016 -0700
|
|     Copy editing for readme (#1)
|
|     * capitalize
|
|     * add punctuation
|
```

## colophon
These git log outputs generated with `git log --graph`
