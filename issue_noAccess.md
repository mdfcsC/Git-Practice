## mdfcsC
*13 minutes ago*

```
vagrant@debian-12:~/project$ git push -u origin master
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

## Copilot
*13 minutes ago*

It looks like you're facing an issue with pushing your code to the GitHub repository due to permission problems. Here are a few steps to resolve this:

1. **Check if you have the correct SSH key added to your GitHub account**
	- Generate a new SSH key if you don't have one: `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
	- Add the generated SSH key to the SSH agent: `ssh-add ~/.ssh/id_rsa`
	- Copy the SSH key to your clipboard: `cat ~/.ssh/id_rsa.pub`
	- Add the SSH key to your GitHub account by navigating to [SSH and GPG keys](https://github.com/settings/keys).

2. **Verify your remote repository URL**
	- Ensure your remote repository URL is using SSH: `git remote set-url origin git@github.com:mdfcsC/Git-Practice.git`

3. **Test the SSH connection to GitHub**
	- Run `ssh -T git@github.com` to check if you can connect to GitHub without any issues.

After checking these steps, try pushing your changes again. If you encounter any issues, feel free to ask for further assistance.

#### Note
You have learnt about setting up ssh keys [here](https://github.com/cs-uob/software-tools/blob/main/01-sysadmin/lab/ssh.md#setting-up-ssh-keys)
