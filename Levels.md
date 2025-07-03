Solutions Walkthrough

Level 0 → 1

Task: Login using SSH.Command:

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Password: Provided on site

Level 1 → 2

Task: Read contents of file named -.

```
cat ./-
```

Level 2 → 3

Task: Read a hidden file in the home directory.
```
ls -a
cat .hidden
```

Level 3 → 4

Task: Find a human-readable file among many with different permissions.
```
ls -l
cat inhere/file2
```

Level 4 → 5

Task: File with specific properties (human-readable, 1033 bytes, not executable).

```
find inhere -type f -size 1033c ! -executable -exec cat {} \;
```

Level 5 → 6

Task: Search for a file with specific permissions.

```
find / -user bandit6 -group bandit5 -size 33c 2>/dev/null -exec cat {} \;
```

Level 6 → 7

Task: Use SSH to login with a password found in a file.

```
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

Level 7 → 8

Task: Find the password stored in a file using grep.

```
grep millionth data.txt
```

Level 8 → 9

Task: Sort and identify a unique line.

```
sort data.txt | uniq -u
```

Level 9 → 10

Task: Decode a password stored in base64 format.

```
base64 -d data.txt
```
