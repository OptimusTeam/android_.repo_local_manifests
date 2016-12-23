Manifest for Android KitKat / CyanogenMod 11.0
====================================
Project M4|L5 / Project U0|L7

Create the Directories:
---

You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin && mkdir -p ~/android/cm11


Install the Repository:
---

Enter the following to download the "repo" binary:

    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect. 
Now enter the following to initialize the repository:

    cd ~/android/cm11

Repositories:
---

Repo Init:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0

To download manifest:

    curl --create-dirs -L -o .repo/local_manifests/manifest.xml -O -L https://raw.githubusercontent.com/OptimusTeam/android_.repo_local_manifests/master/manifest.xml

---

How to use it to use it:

    repo sync --force-sync

---

To get prebuilts

    sh vendor/cm/get-prebuilts

---

Initialize the environment:

    source build/envsetup.sh

---

Make sure to apply patches in device/lge/msm7x27a-common/patches
    
    cd device/lge/msm7x27a-common/patches && ./apply.sh && croot

---

To build for L5:

    brunch e610

---

To build for L7:

    brunch p700

---

To clean repo:

    make clean
