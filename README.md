This is a [VS Code development container](https://github.com/microsoft/vscode-dev-containers) for the [Unison Codebase Manager](https://github.com/unisonweb/unison).

You can check that first link for the full details of how to get set up to use VS Code development containers, but the gist of it is:

1. Install [Docker](https://docs.docker.com/get-docker/).
2. Install the [Remote Development extension pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack).
3. Clone this repo.
4. In VS Code, either:
    - "Open folder..." the cloned repo, then click the "Reopen in container" button that appears in the lower right.
    OR
    - F1 and "Remote-Containers: Open Folder in Container..." the cloned repo.
5. If no terminal appears in VS Code, open a New Terminal from the Terminal menu. 
6. Inside that terminal, run `ucm --codebase-create ./devCodebase` to create a codebase.
7. Run `ui` to start developing!


Your codebase should be persisted even after rebuilding the container, but don't forget to also `push` it somewhere safe as a backup!

Improvements, suggestions, and simplifications are welcome!

Note: when running `ui`, you'll get a message like: 
```
  The Unison Codebase UI is running at
  http://127.0.0.1:39189/LMvqYeofPKwM7uOh5b7A%2FbtEM8tuN%2F%2Fu/ui
```
You should be able to ctrl-click on that link in your terminal to open the UI, but due to a [bug in VSCode](https://github.com/microsoft/vscode/issues/133551), the link will get messed up. Specifically, the `%2F` in the link will be converted to `/`s in your browser. You'll have to copy/paste a bit to get it back to normal, and then it should work.
