# nodejs
This repository contains the files necessary to run a sample application in Node.js and to run CI tests on Shippable.


Contents:
This repository has 6 files and the functions of each file are as follows:

1. README.md - Contains an some basic conventions and guidelines to show the working of folder level caching.
2. Shippable.yml - Configured for the language, version & to run a test during the CI step. http://docs.shippable.com/ci_configure/ gives you a detailed introduction on how to configure your CI on shippable.
3. Package.json - Installs all the libraries mentioned in dependencies list when we run npm install command from the root of this folder. The npm install command createsds a new folder called node_modules which contains all the libraries mentioned in the dependency list.
4. index.js - Outputs "Welcome to Shippable" in a browser
5. test.js - Configured to run a simple unit test to check the syntax of the index.js output
6. Gruntfile.js - grunt file that loads express server and mocha Test
7. xunit.xml - 
8. .gitignore - default file created at the time of creating this repository
hellof the
dd
www
sdsdsd
asdad
sdsd
hello
hello world123gggg
hgsdf
d
123
asdads
1234
asd


## Steps to bring up new machines on rc

### Step 1:
- Pause deploy_rc job

### Step 2: 
- Update Shippable/infra to have new machine (Similiar to this PR https://github.com/Shippable/infra/pull/317/files)

### Step 3:
- Run rc_saas_infra_prov job after your PR is merged. Note down the new machines ip addresses which will show in job consoles at the end of the job.

### Step 4:
- SSH into rc jump box and edit .ssh/config file to have new ip of the machines.

### Step 5:
- Open rc admiral UI from your local and in Swarm section remove old workers and add new ones.
- Copy the command from the box below to authorize ssh access and run this on all the new machine that you initilized by doing SSH into them from rc jumpbox.
- Select the check box when you are done and then Initilize.

### Steo 6:
- Unpause deploy_rc job

When this ends rc should be up and running on new machines.


