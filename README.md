# expo-in-app-purchases-violation-repro
Reproducing Invariant Violation due to expo-in-app-purchases package.

# Commands I ran to build the app
```
$expo init
✔ What would you like to name your app? … test-bare-app
✔ Choose a template: › minimal               bare and minimal, just the essentials to get you started
✔ Downloaded and extracted project files.
🧶 Using Yarn to install packages. Pass --npm to use npm instead.
✔ Installed JavaScript dependencies.

✔ Installed pods and initialized Xcode workspace.

✅ Your project is ready!

To run your project, navigate to the directory and run one of the following yarn commands.

- cd test-bare-app
- yarn android
- yarn ios
- yarn web

💡 You can also open up the projects in the ios and android directories with their respective IDEs.
🚀 expo-updates (​https://github.com/expo/expo/blob/master/packages/expo-updates/README.md​) has been configured in your project. If you publish this project under a different user account than bgodlove88, you'll need to update the configuration in Expo.plist and AndroidManifest.xml before making a release build.

$cd test-bare-app/

$expo install expo-in-app-purchases
Installing 1 SDK 40.0.0 compatible native module using Yarn.
> yarn add expo-in-app-purchases@~9.1.0
yarn add v1.16.0
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
info To upgrade, run the following command:
$ curl --compressed -o- -L https://yarnpkg.com/install.sh | bash
warning Your current version of Yarn is out of date. The latest version is "1.22.5", while you're on "1.16.0".
success Saved 1 new dependency.
info Direct dependencies
└─ expo-in-app-purchases@9.1.0
info All dependencies
└─ expo-in-app-purchases@9.1.0
✨  Done in 5.38s.

$npx pod-install
npx: installed 1 in 1.314s
Scanning for pods...
1.10.1
> pod install
Installing unimodules:
 expo-application@2.4.1 from ../node_modules/expo-application/ios
 expo-constants@9.3.5 from ../node_modules/expo-constants/ios
 expo-error-recovery@1.4.0 from ../node_modules/expo-error-recovery/ios
 expo-file-system@9.3.0 from ../node_modules/expo-file-system/ios
 expo-font@8.4.0 from ../node_modules/expo-font/ios
 expo-image-loader@1.3.0 from ../node_modules/expo-image-loader/ios
 expo-in-app-purchases@9.1.0 from ../node_modules/expo-in-app-purchases/ios
 expo-keep-awake@8.4.0 from ../node_modules/expo-keep-awake/ios
 expo-linear-gradient@8.4.0 from ../node_modules/expo-linear-gradient/ios
 expo-location@10.0.0 from ../node_modules/expo-location/ios
 expo-permissions@10.0.0 from ../node_modules/expo-permissions/ios
 expo-secure-store@9.3.0 from ../node_modules/expo-secure-store/ios
 expo-splash-screen@0.8.1 from ../node_modules/expo-splash-screen/ios
 expo-sqlite@8.5.0 from ../node_modules/expo-sqlite/ios
 expo-updates@0.4.2 from ../node_modules/expo-updates/ios
 unimodules-app-loader@1.4.0 from ../node_modules/unimodules-app-loader/ios
 unimodules-barcode-scanner-interface@5.4.0 from ../node_modules/unimodules-barcode-scanner-interface/ios
 unimodules-camera-interface@5.4.0 from ../node_modules/unimodules-camera-interface/ios
 unimodules-constants-interface@5.4.0 from ../node_modules/unimodules-constants-interface/ios
 unimodules-core@6.0.0 from ../node_modules/@unimodules/core/ios
 unimodules-face-detector-interface@5.4.0 from ../node_modules/unimodules-face-detector-interface/ios
 unimodules-file-system-interface@5.4.0 from ../node_modules/unimodules-file-system-interface/ios
 unimodules-font-interface@5.4.0 from ../node_modules/unimodules-font-interface/ios
 unimodules-image-loader-interface@5.4.0 from ../node_modules/unimodules-image-loader-interface/ios
 unimodules-permissions-interface@5.4.0 from ../node_modules/unimodules-permissions-interface/ios
 unimodules-react-native-adapter@5.7.0 from ../node_modules/@unimodules/react-native-adapter/ios
 unimodules-sensors-interface@5.4.0 from ../node_modules/unimodules-sensors-interface/ios
 unimodules-task-manager-interface@5.4.0 from ../node_modules/unimodules-task-manager-interface/ios

Auto-linking React Native modules for target `testbareapp`: RNGestureHandler, RNReanimated, and RNScreens
Analyzing dependencies
Downloading dependencies
Installing EXInAppPurchases (9.1.0)
Generating Pods project
Integrating client project
Pod installation complete! There are 59 dependencies from the Podfile and 58 total pods installed.
```
