# MDXEditor

## Customization Notes

This codebase is a fork of <https://github.com/mdx-editor>

That project has an optional dependency which introduces a licensing issue.

<https://github.com/mdx-editor/editor/issues/789> documents a licensing problem in the upstream project.

Specifically, an optional package from CodeSandbox:

> MDX editor integrates sandpack within the main package and sandpack dependes on nodebox:
> <https://github.com/Sandpack/nodebox-runtime?tab=License-1-ov-file>
>
> Nodebox has a proprietary custom license which forbids commercial use.
>
> The problem is nodebox allways gets installed when installing mdx editor. Tree shaking will probably kick it out when not used, but thats not 100% sure.
>
> This can theoretically lead to possible legal issues for everyone using it commercially.

Due to this, we need to fork to strip that dependency.

### Changes

This codebase should mirror the existing repo until that licensing issue is resolved.

Do not make arbitrary changes to this repo, since it will make it harder to reconverge.

To that end, this section outlines the deliberate changes

1. Remove sandpack and CodeSandbox PR: <https://github.com/VivaaHealth/mdx-editor/pull/1>
2. Update README: <https://github.com/VivaaHealth/mdx-editor/pull/2>

## Package Notes

![npm](https://img.shields.io/npm/v/@mdxeditor/editor)
![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@mdxeditor/editor)

> Because markdown editing can be even more delightful.

MDXEditor is an open-source React component that allows users to author markdown documents naturally. Just like in Google docs or Notion. [See the live demo](https://mdxeditor.dev/editor/demo) that has all features turned on.
The component supports the core markdown syntax and certain extensions, including tables, images, code blocks, etc. It also allows users to edit JSX components with a built-in JSX editor or a custom one.

```jsx
import { MDXEditor, headingsPlugin } from '@mdxeditor/editor'
import '@mdxeditor/editor/style.css'

export default function App() {
  return <MDXEditor markdown={'# Hello World'} plugins={[headingsPlugin()]} />
}
```

## Get Started

The best place to get started using the component is the [documentation](https://mdxeditor.dev/editor/docs/getting-started).

## Help and support

If you find a bug, check if something similar is not reported already in the [issues](https://github.com/mdx-editor/editor/issues). If not, [create a new issue](https://github.com/mdx-editor/editor/issues/new?assignees=&labels=bug&projects=&template=1.bug.md&title=%5BBUG%5D).

If you're integrating the component in your commercial project and need dedicated assistance with your issues in exchange of sponsorship, [contact me over email](mailto:petyo@mdxeditor.dev).

If you want to discuss ideas start a discussion in the [Discussions](https://github.com/mdx-editor/editor/discussions) section.

## License

MIT &copy; Petyo Ivanov.
