---
sidebar_position: 2
sidebar_label: Roles
---

# Model Roles

Plandex has multiple **roles** that are used for different aspects of its functionality. Each role can have its model and settings changed independently. These are the roles:

### `planner`

This is the 'main' model that replies to prompts and makes plans.

### `summarizer`

Summarizes conversations to stay under the limit set in `max-convo-tokens`. Also keeps track of the status of a plan to help determine whether it's finished or should continue (in conjunction with the `auto-continue` role).

### `auto-continue`

Determines whether a plan is finished or should automatically continue based on the previous response and the `summarizer` role's latest summary.

### `builder`

Builds the proposed changes described by the `planner` role into pending file updates.

### `verifier`

Verifies correctness of file updates produced by the `builder` role. Defaults to the same model and settings as the `builder` role.

### `auto-fix`

Fixes syntax errors, as well as other problems identified by the `verifier` role. Defaults to the same model and settings as the `builder` role.

### `names`

Gives automatically-generated names to plans and context.

### `commit-messages`

Automatically generates commit messages for a set of pending updates.
