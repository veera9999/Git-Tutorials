Hello Fellow Tech Enthusiasts, This is a simple repository to explain how git commands work and make our lives simpler as developers

```
git config --global core.editor "code --wait"
```

This command is used to configure vscode as a default text editor for our git commits, It enables us to write more clear and brief git commits which is generally a good practice especially when you work with a team of developers. Just type this command in your CLI and your git commit text editor will be configured to vscode.

```
Remove-Item -Recurse -Force .git
```

This command will completly remove the git repository in your local system. It will delete the hidden git files in your git repository and breaks the connection between your local repository and remote repsoitory in github.

The Remove-Item -Recurse -Force .git command in PowerShell is used to delete a directory and all of its contents. Here's a breakdown of what each part of the command does:

- Remove-Item: This cmdlet is used to delete items like files, directories, registry keys, variables, aliases, and functions.

- -Recurse: This parameter tells PowerShell to remove the item(s) recursively. This means that if the item is a directory, it will remove all files and subdirectories within that directory.

- -Force: This parameter forces the removal of items that cannot be removed by default. For instance, it can be used to remove read-only files or items that are protected by the system.

- .git: This specifies the target item to be removed, in this case, the .git directory, which is the directory used by Git to store repository data.

## What's actually Happening

- Cmdlet Invocation: PowerShell identifies Remove-Item as a cmdlet and prepares to execute it.

- Parameter Parsing: The parameters -Recurse and -Force are parsed and associated with the Remove-Item cmdlet.

- Item Resolution: PowerShell resolves the .git path to ensure it points to a valid directory or file.

- Recursion Handling: Since -Recurse is specified, PowerShell iterates through all the contents of the .git directory, including all subdirectories and files.

- Force Deletion: With the -Force parameter, PowerShell bypasses any restrictions that would normally prevent the deletion of certain files (e.g., read-only or system-protected files).

- Item Deletion: PowerShell attempts to delete each item it has resolved. If any issues arise (e.g., permission issues, non-existent files), the -Force parameter ensures PowerShell tries to handle these issues and proceed with the deletion.

- Completion: Once all items are processed and removed, the .git directory itself is deleted.

This process ensures that the entire .git directory, including all its contents, is completely removed from the system.
