# vd-tools

Google's tool for converting svg files to Android Vector Drawables.

## Build Instructions
This repo includes a pre-built vd-tool, but it can be built by:

1. [Set up the repo tool](https://source.android.com/source/downloading.html) to get the Android sources
2. cd into an empty directory and run `repo init -u https://android.googlesource.com/platform/manifest -b studio-4.1.1`.  As future versions of AndroidStudio come out, the `studio-4.1.1` tag can be updated.
3. Run this command to start the lengthy step to get the sources: `repo sync -j8 -c`
4. cd into `./tools/base`
5. Run this command to build the tool: `../gradlew publishLocal`

A zip archive containing the same contents as this repo will be available in `out/build/base/vector-drawable-tool/build/distributions/`

With thanks to Alex Lockwood for [these build instructions](https://www.androiddesignpatterns.com/2018/11/android-studio-svg-to-vector-cli.html).

## Usage

```
vd-tool -c -in directory_with_svgs -out directory_that_will_hold_xml
```

