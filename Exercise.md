# Guestbook Exercise

## Before you begin
Make sure you have you SSH key pair configured with the private key on your laptop and the public key saved to your GitHub Account

## Part 1 – Prepare your own guestbook

1. Use the provided template repository to create your own repository:
   - Create it in this organization
   - Name it `guestbook-your-name`
   - Make sure it is public
   - After creation, click the *Code* button and copy the SSH URL

### In the local terminal

2. Clone the repository using the SSH URL you copied:
   ```
   git clone <ssh-url>
   cd guestbook-your-name
   ```

3. Open the repository folder in VS Code and edit README.md:
   - Clear the existing contents
   - Add your own message, for example:
     *Welcome to my guestbook*

4. Add, commit, and push your changes:
    ```
   git add README.md
   git commit -m "Customize guestbook README"
   git push
   ```

5. Refresh the repository on GitHub and verify that your changes are visible.

## Part 2 – Write in someone else’s guestbook

1. Browse the organization and choose someone else’s guestbook repository.

2. Click Fork:
   - Choose your personal GitHub account (not an organization)
   - The fork name can be anything

3. In your fork, click Code and copy the SSH URL

### In the local terminal

4. Clone your fork:
   ```
   git clone <ssh-url>
   cd <repo-name>
   ```

5. Create and switch to a new branch for your greeting:
   ```
   git switch -c greeting
   ```

6. Create a new file inside the guestbook/ folder:
   - File name: <your-name>.md (for example fredrik.md)
   - File contents:
     Hello from Fredrik!

7. Add, commit, and push your branch:
    ```
   git add guestbook/<your-name>.md
   git commit -m "Add greeting from <your name>"
   git push -u origin greeting
   ```

### On GitHub

8. Open your fork on GitHub. You should see a banner suggesting to Create Pull Request:
   - Click Compare & pull request
   - Make sure:
     - Base repository: the original guestbook
     - Base branch: main
     - Head branch: greeting
   - Add a short description
   - Click Create pull request

9. Visit your own guestbook repository:
   - Review any incoming Pull Requests
   - Read the changes
   - Merge them when they look good
