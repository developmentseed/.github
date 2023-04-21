# DevelopmentSeed GitHub Playbook

## Reusing Workflows

In this repository, we store [reusable GitHub Actions workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows).

Recommended reading:

- [Reusing workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows)
- [Creating starter workflows](https://docs.github.com/en/actions/using-workflows/creating-starter-workflows-for-your-organization)
- [Using starter workflows](https://docs.github.com/en/actions/using-workflows/using-starter-workflows)


## Multiple Pull Request templates

As of April 2022, Github doesn't support selecting from a list of PR templates (like it does with issues), but it will load different templates if specified through a query string. (`?template=file.md`)

A possible approach to multiple PR templates is to create a default template ( `PULL_REQUEST_TEMPLATE.md` - which is just a list of links) where you click preview and then can select your options. Example:  

![image](https://user-images.githubusercontent.com/1090606/154232170-c53b8ff3-b8a2-43ed-befe-fc91b4b02e46.png)

<details>
<summary>Code</summary>

```
## Available PR templates

<!--
  Github doesn't allow PR template selection the same way that it is possible with issues.
  Preview this and select the appropriate template:
-->

- [Version Release](?expand=1&template=version_release.md)
- _Alternatively delete and start empty_
```

</details>

All the other templates go inside the `PULL_REQUEST_TEMPLATE` directory. Each template should be a markdown file, whose filename you'll have to add to the list of links in the default template.


Here's a quick video demonstrating the flow.

https://user-images.githubusercontent.com/1090606/154234453-06adb23a-48e1-489c-9849-134fab1ceec4.mov

## Issue 1 Template
There's an Issue 1 template that can be used across any repositories in our Github account. Issue 1s are used to keep track of new projects and phases.

Here's how you can use it. In a repo, click Issues > New Issue > Issue 1

![issue-1-usage](https://user-images.githubusercontent.com/371666/233577660-c19c8ed7-8eb8-44b2-a050-ea002ed72bff.gif)
