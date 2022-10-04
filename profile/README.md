# Data analytics team

Welcome! 

This organization stores main projects developed by the **re.green**'s data analytics team. 

Good practices adapted by our team

- repositories should be self-contained and whenever is possible use relative paths to read and write data
- always use `git pull` and `git push` to avoid conflicts
- for repositories with branches (e.g. `cf_refor`), work on branch `dev` and keep the `main` updated from time to time
- always create a `README.md` explaining the context of the project
- specify which libraries and data are needed for each project
- for collective commits use: 

```
Your commit message followed by two vertical spaces.


Co-authored-by:
username <user@email.com>
```

## Adding a new user on RStudio server

```
sudo useradd -m usuario
sudo passwd usuario

sudo usermod -a -G regreen,rstudio-server,sshusers usuario
```

If it doesn't work, then

```
sudo mkdir /home/usuario
chown -R usuario:usuario /home/usuario
```

Format `home/.Renviron` to have the following lines:

R_USER = /PROC/rtmp/
R_LIBS_USER = /DATA/libraryR/4.1/

