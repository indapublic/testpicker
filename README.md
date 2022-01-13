How to reproduce:

```bash
npx react-native init testpicker --template react-native-template-typescript --npm
npm install --save @react-native-picker/picker
cd android
./gradlew build
```

Result:

```
> Task :react-native-picker_picker:lint FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':react-native-picker_picker:lint'.
> Lint found errors in the project; aborting build.

  Fix the issues identified by lint, or add the following to your build script to proceed with errors:
  ...
  android {
      lintOptions {
          abortOnError false
      }
  }
  ...
  Errors found:

  /private/tmp/testpicker/node_modules/@react-native-picker/picker/android/src/main/java/com/reactnativecommunity/picker/CheckedTextViewImpl.java:7: Error: This custom view should extend androidx.appcompat.widget.AppCompatCheckedTextView instead [AppCompatCustomView]
  public class CheckedTextViewImpl extends CheckedTextView {
                                           ~~~~~~~~~~~~~~~
  /private/tmp/testpicker/node_modules/@react-native-picker/picker/android/src/main/java/com/reactnativecommunity/picker/TextViewImpl.java:7: Error: This custom view should extend androidx.appcompat.widget.AppCompatTextView instead [AppCompatCustomView]
  public class TextViewImpl extends TextView {
                                    ~~~~~~~~
```