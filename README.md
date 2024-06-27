### File Permissions in Linux

#### Project Description
This document outlines the steps to manage and modify file permissions using Linux commands. As a security professional, ensuring that users have the appropriate permissions is crucial for maintaining the system's security.

#### Check File and Directory Details
To examine existing file and directory permissions, use the `ls -l` command. This command lists the details of files and directories, including their permissions.

Example:
```sh
ls -l /home/researcher2/projects
```
Output:
```
-rw-rw-r-- 1 user group 2048 Jun 27 14:33 project_k.txt
-rw-r----- 1 user group 1024 Jun 27 14:33 project_m.txt
-rw-rw-r-- 1 user group 2048 Jun 27 14:33 project_r.txt
-rw-rw-r-- 1 user group 2048 Jun 27 14:33 project_t.txt
-rw-rw---- 1 user group 1024 Jun 27 14:33 .project_x.txt
drwx--x--- 2 user group 4096 Jun 27 14:33 drafts
```
![Screenshot 2024-06-28 092553](https://github.com/jenriquez00/File-Permissions-in-Linux/assets/167884340/115162b5-33bd-4258-a0b3-9e71f6e83edc)

#### Describe the Permissions String
The permissions string in the output from `ls -l` consists of 10 characters. The first character represents the file type (e.g., `-` for regular files, `d` for directories). The next nine characters are divided into three groups, each representing permissions for the user, group, and others, respectively.

For example, in the string `-rw-rw-r--`:
- `-` indicates a regular file.
- `rw-` means the user has read and write permissions.
- `rw-` means the group has read and write permissions.
- `r--` means others have read-only permissions.

#### Change File Permissions
To change file permissions, use the `chmod` command. This command can modify the permissions for the user, group, and others.

Example:
```sh
chmod 644 /home/researcher2/projects/project_k.txt
```
This command changes the permissions of `project_k.txt` to `rw-r--r--`.

#### Change File Permissions on a Hidden File
Hidden files in Linux start with a dot (`.`). The same `chmod` command can be used to modify permissions for hidden files.

Example:
```sh
chmod 640 /home/researcher2/projects/.project_x.txt
```
This command changes the permissions of `.project_x.txt` to `rw-r-----`.

#### Change Directory Permissions
To change the permissions of a directory, use the `chmod` command with the appropriate options.

Example:
```sh
chmod 750 /home/researcher2/projects/drafts
```
This command changes the permissions of the `drafts` directory to `rwxr-x---`.

#### Summary
In this activity, you learned how to check and modify file and directory permissions using Linux commands. By ensuring that the permissions are correctly set, you help maintain the security and integrity of the system. This document demonstrates your ability to manage file permissions, a crucial skill in cybersecurity.

### Example of a Portfolio Document on GitHub

You can create a new repository on GitHub and add a README.md file with the above content. Here's a sample structure for your repository:

```
GitHub Repository: linux-file-permissions
│
├── README.md
└── images
    ├── file_permissions.png
    └── directory_permissions.png
```

#### README.md
```markdown
# Managing File Permissions in Linux

## Project Description
This document outlines the steps to manage and modify file permissions using Linux commands. As a security professional, ensuring that users have the appropriate permissions is crucial for maintaining the system's security.

## Check File and Directory Details
To examine existing file and directory permissions, use the `ls -l` command. This command lists the details of files and directories, including their permissions.

![File Permissions](images/file_permissions.png)

## Describe the Permissions String
The permissions string in the output from `ls -l` consists of 10 characters. The first character represents the file type (e.g., `-` for regular files, `d` for directories). The next nine characters are divided into three groups, each representing permissions for the user, group, and others, respectively.

## Change File Permissions
To change file permissions, use the `chmod` command. This command can modify the permissions for the user, group, and others.

```sh
chmod 644 /home/researcher2/projects/project_k.txt
```

## Change File Permissions on a Hidden File
Hidden files in Linux start with a dot (`.`). The same `chmod` command can be used to modify permissions for hidden files.

```sh
chmod 640 /home/researcher2/projects/.project_x.txt
```

## Change Directory Permissions
To change the permissions of a directory, use the `chmod` command with the appropriate options.

```sh
chmod 750 /home/researcher2/projects/drafts
```

## Summary
In this activity, you learned how to check and modify file and directory permissions using Linux commands. By ensuring that the permissions are correctly set, you help maintain the security and integrity of the system. This document demonstrates your ability to manage file permissions, a crucial skill in cybersecurity.
```

Don't forget to add screenshots of your commands and their outputs in the `images` folder and reference them in the README.md file. This will provide a visual demonstration of your work.
