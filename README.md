this is only for save working vab with 
``` 
cd ~/.vmodules/raylib/raylib/src
make clean
make PLATFORM=PLATFORM_ANDROID \
     ANDROID_NDK=$ANDROID_NDK_HOME \
     ANDROID_ARCH=arm64 \
     ANDROID_API_VERSION=21 \
     INCLUDE_PATHS="-I$ANDROID_NDK_HOME/sources/android/native_app_glue \
                    -I$ANDROID_NDK_HOME/toolchains/llvm/prebuilt/linux-x86_64/sysroot/usr/include \
                    -I$ANDROID_NDK_HOME/toolchains/llvm/prebuilt/linux-x86_64/sysroot/usr/include/aarch64-linux-android"
~/v$ ../.vmodules/vab/vab --archs "arm64-v8a" -v 3 --no-parallel ./examples/hello.v 

```
in "v" is working apk for arm64
