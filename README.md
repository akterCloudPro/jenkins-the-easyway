# jenkins-the-easyway


### Few error and fix
- docker login fails on a server with no X11 installed
  Looks like this is because it defaults to use the secretservice executable which seems to have some sort of X11 dependency for some reason. If you install and configure pass   docker will use that instead which seems to solve the problem.

In a nutshell (from https://github.com/docker/compose/issues/6023)

- sudo apt install gnupg2 pass 
- gpg2 --full-generate-key
