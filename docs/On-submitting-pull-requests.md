## Choosing the right base branch

The WRC operates with two branches:
  - `draft` is the current work-in-progress branch, and where any new Regulations change will land
  - `official` is the current official version of the WCA Regulations and Guidelines. When a new release of the Regulations is created, the WRC merges the current `draft` into `official`.

If your pull request adresses only minor changes, without an influence of the Regulations meaning, then it is known as a *textual revision*, and should be submitted using **`official`** as the base branch.

If it adresses anything else, please submit it using **`draft`** as the base branch.

We need to make textual revisions against `official` because once the changes are merged into `official`, the WRC will merge `official` into `draft` to port your changes to the current work-in-progress version.
It's necessary, as doing it the other way around (merging first in `draft`, then backporting to `official`) would also bring all the current major changes from `draft` to `official`, which is definitely not something we want.
Other options (such as cherry-picking) are not viable, as we want `draft` and `official` to share the same history (and not rewrite it!).