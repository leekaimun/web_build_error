# Flutter web error on AppBar with FlexibleSpace and TabBar

While running the flutter app from the browser, the AppBar that contain FlexibleSpace and TabBar failed to render with javascript errors.

## Environment
```
~$ flutter doctor -v

[✓] Flutter (Channel stable, 2.2.0, on Linux, locale en_SG.UTF-8)
    • Flutter version 2.2.0 at /opt/flutter
    • Framework revision b22742018b (2 weeks ago), 2021-05-14 19:12:57 -0700
    • Engine revision a9d88a4d18
    • Dart version 2.13.0

[✓] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
    • Android SDK at /home/lawrence/Android/Sdk
    • Platform android-30, build-tools 30.0.3
    • Java binary at: /usr/local/android-studio/jre/bin/java
    • Java version OpenJDK Runtime Environment (build 11.0.8+0-b944-P17168821)
    • All Android licenses accepted.

[✓] Chrome - develop for the web
    • Chrome at google-chrome

[✓] Android Studio (version 4.2)
    • Android Studio at /usr/local/android-studio
    • Flutter plugin version 56.0.2
    • Dart plugin version 202.8488
    • Java version OpenJDK Runtime Environment (build 11.0.8+0-b944-P17168821)

[✓] Android Studio
    • Android Studio at /home/lawrence/android-studio
    • Flutter plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/9212-flutter
    • Dart plugin can be installed from:
      🔨 https://plugins.jetbrains.com/plugin/6351-dart
    • Java version OpenJDK Runtime Environment (build 11.0.8+0-b944-P17168821)

[✓] VS Code (version 1.56.2)
    • VS Code at /usr/share/code
    • Flutter extension version 3.22.0

[✓] Connected device (1 available)
    • Chrome (web) • chrome • web-javascript • Google Chrome 90.0.4430.212

• No issues found!
```
## Building the application

    $ flutter build web --profile

## Observing the error

Use a web server to serve the web pages built in folder "build/web" and use any browser to load the index.html.

The javascript error shown on Chrome console is as follows:

    NoSuchMethodError: method not found: 'get$value' on null
