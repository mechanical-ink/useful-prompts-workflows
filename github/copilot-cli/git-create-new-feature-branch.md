# Prompt GitHub Copilot for CLI to Create A New Feature Branch

Not _everything_ happens on GitHub, so sometimes, we do not have the nifty tools GitHub provides to create a new feature branch from an issue easily. You may use Shortcut, Linear, ClickUp, or other project management tools. The following prompt lets you easily create a new feature branch using the specified `id` and `description`.

Let's say there is an issue with an `id` of `4668`, and the issue has the following title:

> Search - Add "Show Results" button to bottom of the left side filter

There are a few things in this description that can be tricky. It contains a dash, double quotes, and spaces between the words. The following prompt has consistently given me the exact result I wanted.

```bash
git? using git switch, create a new feature branch with the id [id] and the name: [description]. Remember to replace spaces with dashes and remove any special characters from the branch name. Please also lowercase everything in the branch name.
```

When run, Copilot will suggest something like the following based on the earlier example:

```bash
git switch -c 4734-search-add-show-results-button-to-bottom-of-the-left-side-filter
```

Execute it, and you are off to the races.
