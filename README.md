CM11 Manifests
========================
Project Vee3 / Project V1

Local manifests to build Android LolliPop 5.1 to L3II and L1II

To initialize CM12.1 Repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-12.1 -g all,-notdefault,-darwin

To initialize Repo's:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/TeamVee/android_.repo_local_manifests/cm-12.1/local_manifest.xml

To sync:

    repo sync

To apply patchs:

    sh device/lge/vee3/patches/apply.sh

To initialize the environment

    . build/envsetup.sh

To build for L3 II:

    brunch vee3

To build for L1 II:

    export TARGET_KERNEL_V1_BUILD_DEVICE=true
    brunch vee3
