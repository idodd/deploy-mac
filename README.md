## Before beginning


Are you doing this for the first time? If yes, **please take notes** on anything that doesn't work as described, and update this document with any adjustments, cautions, or lessons learned.

_These instructions are tested for Mac OS X Sierra (10.12.4)_

### Get yourself briefed

Please take a moment to review our [Information Technology and Security policies]


## System preparation

### OSX

1. Check if Xcode Command Line Tools is installed. If not: 
```
$ xcode-select --install
  # You may need to sign in with your Apple ID.
```

### GitHub

1. [Generate an RSA key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) if you don't already have one
1. [Add your SSH key to your GitHub account.](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

### Ansible

Our Ansible playbook should automatically install all the other apps and packages you'll need. 

**First, install Ansible locally:**

```
$ sudo easy_install pip
$ sudo pip install ansible==1.9.4 --quiet
```

**Get our playbook:**

1. Visit the [deploy-mac repository](https://github.com/.........) on GitHub.
1. DO NOT CLONE THE REPO. Download it from the github page and unzip it.
1. Navigate into the folder.
1. Run the playbook (and stay close, you may need to enter your password a couple of times): 

```
$ ansible-playbook local/local.yml -i local/HOSTS --ask-sudo-pass
```

**Add your SSH public key to the deploy-mac repo:**

1. Put your SSH key file and path into deploy-mac.

**Finally, restart your shell** to load new environment variables.
