# Cursor Rules

These rules are designed for the [Cursor IDE](https://cursor.com/) following their [documentation](https://docs.cursor.com/context/rules)

## Determining When to Apply Rules

The front matter at the top of each rule file determines how the file gets applied. 
How to configure this is listed in the table below (credit to this [blog post](https://apidog.com/blog/awesome-cursor-rules/#setting-up-and-using-project-rules))

**NOTE: This front matter does not appear in Cursor. You must edit it in a different text editor to be able to modify it**

| RULE TYPE | METADATA SETTINGS | DESCRIPTION |
|-----------|-------------------|-------------|
| `Always` | `alwaysApply: true` | Always included in the model context for the project. |
| `Auto Attached` | `globs: ["pattern"]`, `alwaysApply: false` | Included *only* when files matching the `globs` pattern are part of the AI's context (e.g., in chat). |
| `Agent Requested` | `description: "..."`, `alwaysApply: false` | The rule is *available* to the AI, which decides whether to fetch and use it based on the `description`. |
| `Manual` | `alwaysApply: false` (or omitted) | Only included when explicitly mentioned in chat using `@ruleName` (e.g., `@django-style`). |

## Testing Prompts

Prompts we use to test the rules to see how they perform.

```
Build a Temporal application using the Python SDK that allows the user to submit text and the application posts that text to their X, Bluesky, and Mastodon account. 
```

**We're still learning as well. PRs and new rules very welcome!**
