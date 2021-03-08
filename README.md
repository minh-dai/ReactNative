- Tao moi project: 
	react-native init HelloWorld
	react-native init newproject --version react-native@0.59.9

-- All : https://github.com/react-native-community
-- gitgnore: https://stackoverflow.com/questions/1139762/ignore-files-that-have-already-been-committed-to-a-git-repository
	

- ThÙng b·o v‡ animation : https://github.com/react-native-community/react-native-modal

- Splash Screen: https://github.com/crazycodeboy/react-native-splash-screen

- Dialog: https://www.npmjs.com/package/react-native-dialog
	  https://reactnativeexample.com/tag/dialog/

- bottom sheet: yarn add react-native-raw-bottom-sheet

 -- keyboard: https://www.youtube.com/watch?v=J1yKq_d7O8U&list=PLWBrqglnjNl31S91FFE63DtuRc9v9LSGl&index=62

- redux :  react-native install redux
 	   react-native install react-redux
		npm install redux-thunk
- choose image from device: 
	multiple image: https://github.com/ivpusic/react-native-image-crop-picker

	yarn add react-native-image-picker
	react-native link react-native-image-picker

- animation dep: 
		https://github.com/react-native-community/lottie-react-native
     xoay tron:	https://stackoverflow.com/questions/47911256/react-native-circle-transform-translate-animation
		https://github.com/archriss/react-native-snap-carousel

tool : https://code.tutsplus.com/vi/articles/tools-for-react-native-development--cms-29791

- custom createBottomTabBar: 
	https://github.com/octopitus/rn-sliding-up-panel

	https://reactnativeexample.com/a-beautiful-and-customizable-material-design-bottom-navigation-for-react-native/
-- nhieu animation lam: ngay tren lun nhe

- Prop-Types: https://viblo.asia/p/check-kieu-trong-react-voi-proptypes-07LKX20elV4
-- audio, mËiaPlayer, music : 
	https://github.com/react-native-kit/react-native-track-player
	https://github.com/lufinkey/react-native-spotify


-paper huong dan su dung app: https://github.com/FuYaoDe/react-native-app-intro

- hon 30 ui: https://avocode.com/nachos-ui/docs/#!/Showcase/Indicator

chmod -R 777 ./gradlew 
./gradlew assembleRelease
./gradlew clean

cd android && gradlew assembleRelease

import androidx.localbroadcastmanager.content.LocalBroadcastManager;
import androidx.core.app.RemoteInput;

"react-native-track-player": "^1.1.8",
"react-native-volume-control": "^1.0.1",

- white screen : https://github.com/wix/react-native-navigation/issues/2358


chart: https://medium.com/the-react-native-log/animated-charts-in-react-native-using-d3-and-art-21cd9ccf6c58

Flatlist in ScrollView:
<View>
  <ScrollView removeClippedSubviews={false}>
    <View>
      <SwiperFlatList>
      </SwiperFlatList>
    </View>
    //Your other stuff go here that need scrollview
  </ScrollView>
</View>

Custom bottomTabBar: https://stackoverflow.com/questions/54642226/custom-tabs-styling-on-react-navigation/54644386


react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res

------------------------  OR ---------------------
npx react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res

----------- 
Gitignore not ignoring some build files in Android library

git rm -r --cached .
git add .
git commit -m ".gitignore is now working"

--- Log file in commit
git diff-tree --no-commit-id --name-only -r bd61ad98

git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "MY_NAME@example.com"


# eventx-visitorapp

- faceId wrong in android(samsung)
path: /node_modules/expo-local-authentication/android/src/main/java/expo/modules/localauthentication
change:

if (mPackageManager.hasSystemFeature("android.hardware.biometrics.face") || mPackageManager.hasSystemFeature("com.samsung.android.bio.face")) {
        results.add(AUTHENTICATION_TYPE_FACIAL_RECOGNITION);
      }

path: /node_modules/react-native-swipe-gestures/index.js
change:

      _gestureIsClick(gestureState) {
    return (
      Math.abs(gestureState.dx) < swipeConfig.gestureIsClickThreshold
       //&& Math.abs(gestureState.dy) < swipeConfig.gestureIsClickThreshold
    );
  }

- Image not show

OPEN THE FILE FROM :
node_modules/react-native/Libraries/Image/RCTUIImageViewAnimated.m

if (_currentFrame) {
layer.contentsScale = self.animatedImageScale;
layer.contents = (__bridge id)_currentFrame.CGImage;
} else {
[super displayLayer:layer];
}

- Datepicker is white

<key>UIUserInterfaceStyle</key>
	<string>Light</string>
	<key>UIViewControllerBasedStatusBarAppearance</key>
