### Multi-OS-Engine
---
https://software.intel.com/en-us/inde-eol

https://github.com/moe-java-samples

https://doc.multi-os-engine.org/multi-os-engine/3_getting_started/2_moe_samples/MOE_samples.html

https://github.com/multi-os-engine/multi-os-engine

```sh
mkdir ~/bin
PATH=~/bin:$PATH
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo

brew install repo

repo init -u https://github.com/multi-os-engine/manifest.git
repo sync

repo init -u https://github.com/multi-os-engine/manifest.git -b moe-windows-bitcode
repo sync

brew tap homebrew/versions
brew install autogen autoconf automake libtool pkg-config wget gcc@5 cloog cmake jasmin gpg ant maven

cd <repo>/moe/moe-core
brew install file://`pwd`/dependencies/premake5.rb

cd <repo>/prebuilts
./gradlew mingw llvm

cd <repo>/moe/moe-core
./gradlew build

cd <repo>/moe/tools/master
./gradlew :moe-sdk:devsdk

cd <repo>/moe/tools/master
./gradlew :moe-gradle:publishToMavenLocal

cd <repo>/moe/tools/moe.plugin.maven
mvn clean install

cd <repo>/moe/tools/master
./gradlew :moe.plugin.idea:build

cd <repo>/tools/moe.plugin.eclipse
mvn clean install -DBUILD_NUMBER=1
```

```
```

```
```

