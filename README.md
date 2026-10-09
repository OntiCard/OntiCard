<h1 align='center'>Mabel Nolan</h1>

| | |
|:--|:--|
| GitHub | `@OntiCard` |
| Pronouns | she/her |
| Location | Dublin · `Europe/Dublin` |
| Work | Independent technical writer for developer tools |
| Current surfaces | API reference, onboarding guides, CLI output |

> Good docs are not shorter because the product is easy. They are shorter because someone removed the dead ends.

## How I like to work

I treat documentation as part of the product interface, not a rescue layer placed underneath it. My favourite reviews happen on the pull request, attached to the exact sentence or line break where a reader might stall. A vague comment such as "make this clearer" does not help much; a note like "this assumes the reader already created an API token" gives me something to fix.

For a tricky endpoint or stateful CLI flow, I will ask for twenty minutes with the engineer before drafting. After that, I work better asynchronously: read the code, try the request, break the example, then return with questions.

| I prefer | Why it helps |
|:--|:--|
| Comments on the exact line | The context stays with the wording |
| Error message plus user goal | We can write a real next step |
| One onboarding path per guide | It stops the intro becoming an encyclopedia |
| Docs reviewed in the same PR as code | The interface and explanation cannot drift apart |

## The path here

I came to this work through support tickets. Week after week, the same confusion appeared in slightly different wording: people could authenticate, but they did not know which object came next; the API reference listed every parameter, but the first successful call still felt like a riddle. I started turning those repeated tickets into internal runbooks, then public guides, and eventually into edits to the CLI messages themselves.

Learning OpenAPI involved breaking a great many examples. That was useful. A generated reference can look complete while hiding the practical sequence a new reader needs: create a project, find the right identifier, check the token scope, send the request, interpret the failure.

That curiosity also spilled into a slow blog about open-source license histories. I am less interested in hot takes than in the quiet provenance of a clause, a project rename, or a dependency that outlived its original steward.

## Two questions I keep asking

First, if a reader pastes the first example into a terminal, what is the first thing that tells them it failed? A missing environment variable, expired token, or insufficient scope should not send them searching through raw HTTP status tables. The reference needs to connect the error object to the next command.

Second, what changes in the CLI between an interactive terminal and `--format json`? Progress notes and friendly tables can be useful for a human, but machine-readable output needs stable field names, honest exit codes, and no decorative prose in the middle of a pipe.

```text
curl request -> token scope -> sample response -> error object -> next command
```

Those questions matter because the smallest wording decision often determines whether someone can automate the tool confidently.

## Outside the docs

Most weekends I walk along the Dodder and return with pockets full of unrelated thoughts. At home, I am teaching myself SVG by drawing county-line maps of Ireland: one path at a time, too many control points, occasional arguments with a coastline. It is a useful complement to docs work. Both reward patience, accurate boundaries, and labels placed where a person will actually look for them.
