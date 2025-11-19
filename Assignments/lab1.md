---

# LAB1.md – Linux Basics

## Objective

Practice essential Linux commands from Unit-1 labs (Lab 3 and Lab 5).

---

## Lab Files Chosen

* **Lab 3:** Basic Commands
* **Lab 5:** User & Group Management

---

## LAB 3 – Basic Commands

### 1. Navigation Commands

#### a) `pwd`

```bash
pwd
```

**Sample Output:**
`/home/yourusername/Unit-1`

**Explanation:**
`pwd` shows the current working directory. Helps confirm where you are before running other commands.

---

#### b) `ls`

```bash
ls
```

**Sample Output:**
`Lab3.txt  Lab5.txt`

**Explanation:**
Lists files and directories in the current folder.

---

#### c) `cd`

```bash
cd ..
```

**Sample Output:**
(No output – moves you up one folder.)

**Explanation:**
Changes the current directory. `cd ..` moves one step up, while `cd foldername` moves into a specific folder.

---

### 2. File & Directory Management

#### a) `mkdir`

```bash
mkdir test_folder
```

**Explanation:** Creates a new directory.

---

#### b) `touch`

```bash
touch file1.txt
```

**Explanation:** Creates an empty file (or updates its timestamp if it already exists).

---

#### c) `cp`

```bash
cp file1.txt file2.txt
```

**Explanation:** Copies file1.txt to file2.txt.

---

#### d) `mv`

```bash
mv file2.txt test_folder/
```

**Explanation:** Moves (or renames) files/directories.

---

#### e) `rm`

```bash
rm file1.txt
```

**Explanation:** Deletes a file. Use `rm -r foldername` for directories.

---

### 3. File Viewing & Editing

#### a) `cat`

```bash
cat file2.txt
```

**Explanation:** Displays the contents of a file on the screen.

---

#### b) `nano`

```bash
nano file2.txt
```

**Explanation:** Opens the file for editing using Nano text editor.

---

#### c) `clear`

```bash
clear
```

**Explanation:** Clears the terminal screen.

---

### 4. System Commands

#### a) `echo`

```bash
echo "Hello World"
```

**Explanation:** Prints text or variables to the screen.

---

#### b) `whoami`

```bash
whoami
```

**Explanation:** Displays the current logged-in username.

---

#### c) `man`

```bash
man ls
```

**Explanation:** Opens the manual page for `ls`, showing its usage and options.

---

### 5. Searching & Finding

#### a) `find`

```bash
find . -name "file2.txt"
```

**Explanation:** Searches for a file by name in the current directory (and subdirectories).

---

#### b) `grep`

```bash
grep "Hello" file2.txt
```

**Explanation:** Searches for a word or pattern inside a file.

---

## LAB 5 – User & Group Management

### 1. Create a New User

```bash
sudo useradd -m newuser
```

**Explanation:**
Creates a new user with a home directory `/home/newuser`.

---

### 2. Create a New Group

```bash
sudo groupadd newgroup
```

**Explanation:**
Creates a new group named `newgroup`.

---

### 3. Add User to Group

```bash
sudo usermod -aG newgroup newuser
```

**Explanation:**
Adds `newuser` to `newgroup`. `-aG` ensures the user keeps membership in existing groups.

---

### 4. Create a File and Check Ownership

```bash
touch testfile.txt
ls -l testfile.txt
```

**Sample Output:**

```
-rw-r--r-- 1 youruser youruser 0 Sep 10 14:02 testfile.txt
```

**Explanation:**
Creates a file named `testfile.txt`. `ls -l` shows its owner (your current user) and permissions.

---

### 5. Change Ownership

```bash
sudo chown newuser:newgroup testfile.txt
```

**Explanation:**
Changes the file’s owner to `newuser` and group to `newgroup`.

---

### 6. Verify Ownership

```bash
ls -l testfile.txt
```

**Sample Output:**

```
-rw-r--r-- 1 newuser newgroup 0 Sep 10 14:02 testfile.txt
```

**Explanation:**
Confirms that ownership has been updated successfully.

---

## Extra Questions

### 1. Difference between `chmod` and `chown`

| Command   | Purpose                                                            | Example                           |
| --------- | ------------------------------------------------------------------ | --------------------------------- |
| **chmod** | Changes permissions (read, write, execute) of a file or directory. | `chmod 755 file.txt`              |
| **chown** | Changes ownership of a file or directory (user and/or group).      | `chown newuser:newgroup file.txt` |

---

### 2. How to Check Current Directory & User

* **Current Directory:** `pwd`
* **Current User:** `whoami`

---



