# 02-04-2025
Template Mental Health

My first line


Great! Let's go step by step and use a **README.md** file as our first example.

---

### **Step 1: Create a Project Folder**
1. Open Git Bash and navigate to where you want to store your project.
   ```bash
   cd path/to/your/directory
   ```
   Example:
   ```bash
   cd C:/Users/YourUsername/Documents/WebTemplate
   ```
2. Create a new folder for your website template:
   ```bash
   mkdir my-website-template
   ```
3. Move into the new project folder:
   ```bash
   cd my-website-template
   ```

---

### **Step 2: Initialize Git**
Inside your project folder, initialize Git:
```bash
git init
```
This sets up Git in your project and creates a hidden `.git` folder to track changes.

---

### **Step 3: Create a README.md File**
A `README.md` file is used to describe your project. Let's create one:
```bash
echo "# My Website Template" > README.md
```
This command creates a file named `README.md` with a title inside.

To check if the file exists, run:
```bash
ls
```
You should see `README.md` listed.

---

### **Step 4: Check the Status**
Now, let’s check what Git sees:
```bash
git status
```
Git will say:
```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
  README.md
```
This means `README.md` exists but isn’t tracked yet.

---

### **Step 5: Add the File to Staging (`git add`)**
Now, let's stage the file:
```bash
git add README.md
```
To confirm, run:
```bash
git status
```
Now Git will say:
```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  new file:   README.md
```
The file is now **staged**, meaning it's ready to be saved.

---

### **Step 6: Commit the File (`git commit`)**
Now, let's save our changes:
```bash
git commit -m "Added README file"
```
Git will respond with something like:
```
[main (root-commit) abc1234] Added README file
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```
Your file is now **saved locally**.

---

### **Step 7: Create a GitHub Repository**
1. Go to [GitHub](https://github.com) and log in.
2. Click the **+ (New Repository)** button.
3. Name it **my-website-template** (or whatever you want).
4. **Do NOT initialize with a README** (we already have one).
5. Click **Create Repository**.
6. GitHub will show instructions. Copy the HTTPS URL (e.g., `https://github.com/your-username/my-website-template.git`).

---

### **Step 8: Connect GitHub Repository (`git remote add origin`)**
Now, we need to connect our local project to GitHub:
```bash
git remote add origin https://github.com/your-username/my-website-template.git
```
To verify, run:
```bash
git remote -v
```
You should see something like:
```
origin  https://github.com/your-username/my-website-template.git (fetch)
origin  https://github.com/your-username/my-website-template.git (push)
```

---

### **Step 9: Push the Commit to GitHub (`git push`)**
Now, let’s send our work to GitHub:
```bash
git push -u origin main
```
If this is your first time pushing, Git might ask for your **GitHub username and password**.

Once done, check your GitHub repository—your `README.md` file should be there! 🎉

---

### **Step 10: Edit README and Pull the Latest Changes (`git pull`)**
1. Open `README.md` and change it to:
   ```
   # My Website Template
   This is a simple website template.
   ```
2. Save the file.
3. Check Git status:
   ```bash
   git status
   ```
   Git will say:
   ```
   modified: README.md
   ```
4. Add and commit the change:
   ```bash
   git add README.md
   git commit -m "Updated README with description"
   ```
5. Push the change:
   ```bash
   git push origin main
   ```

Now, imagine you or someone else made changes to the README file **directly on GitHub**. To get the latest version, run:
```bash
git pull origin main
```
This ensures your local copy is **up to date** with GitHub.

---

### **Step 11: Revert to a Previous Version (`git revert`)**
What if you want to undo a change?

1. See the commit history:
   ```bash
   git log --oneline
   ```
   You’ll see something like:
   ```
   3f5e8b2 Updated README with description
   abc1234 Added README file
   ```
2. Revert to the previous version:
   ```bash
   git revert 3f5e8b2
   ```
3. Git will ask you to confirm. Type `:wq` (write & quit) and press **Enter**.

Now, the latest change is undone, and you can push it:
```bash
git push origin main
```

---

### **Summary of Commands**
| Command | What It Does |
|---------|-------------|
| `git init` | Initialize a Git repo |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save changes locally |
| `git remote add origin URL` | Connect to GitHub |
| `git push origin main` | Upload changes to GitHub |
| `git pull origin main` | Get the latest changes from GitHub |
| `git log --oneline` | View commit history |
| `git revert <commitID>` | Undo a commit |

---

This is the basic workflow you'll use when building your website template! Want to try adding an **index.html** file next? 😊