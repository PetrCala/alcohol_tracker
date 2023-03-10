==================================================
Devloper documentation
==================================================


This is the main documentation for running the project.


Prerequisites
================================

#. Install `node.js <https://nodejs.org/>`_.
#. Install the `Java SE Development Kit (JDK)  <https://www.oracle.com/java/technologies/downloads/#java17>`_. We recommend you use the long-term-supported version 17. After the installation, open the *Edit environment variables for your account* window from the Windows control pannel, and ADD a new variable named *JAVA_HOME*. Set its value to the installed folder of the JDK (most likely :code:`C:\\ProgramFiles\\Java\\jdk-{version-name}\\`)
#. Install React Native by running :code:`npx react native`


Setting up the project after cloning the repository
================================
#. Install all dependencies using :code:`npm i`.


Setting up the project from scratch
================================

#. If you need to set up the project from scratch (not clone it from the GitHub repository), we recommend you follow the `official documentation <https://reactnative.dev/docs/environment-setup>`_.
    * Initialize the project using :code:`npx react-native init alcohol_tracker --template react-native-template-typescript --npm`
    * It is good to keep the best practice when it comes to folder organization. Please keep in line with the GitHub folder structuring when recreating the project from scratch.


Running the application using an emulator
================================

#. To start the bundler, go inside the project directory, and run :code:`npm start`.
#. Install an emulator in your machine:
    * Android: We recommend you use `Android Studio <https://developer.android.com/studio>`_. Set up the android studio using the `official React Native documentation <https://reactnative.dev/docs/environment-setup>`_, and create an emulator device.
#. Start up the emulator device.
#. You can run the application in the Android environent by using :code:`npm run android` from the project root directory.
#. If all went right, you should see the application open in the emulator device.


Running the application on an Android device
================================

#. You can follow the official documentation for setting up the Android environment `here <https://reactnative.dev/docs/running-on-device>`_.
#. Make sure the Android Debug Bridge is traceable by your computer. This means putting the :code:`Android\\sdk\\platform_tools\\` folder into your system PATH.
#. Connect your Android device to your computer using a USB cable.
#. Enable USB debugging on your device by going to :code:`Settings\\Developer options\\USB debugging`.
#. Check that your computer is able to detect the device by running :code:`adb devices`. If it is not, try checking `here <https://stackoverflow.com/questions/21170392/my-android-device-does-not-appear-in-the-list-of-adb-devices>`_.
#. In your project directory, run the command :code:`npm run android`. This will start the Metro bundler and build your app.
#. When the build is complete, your app will be installed and launched on your connected device automatically.
    * Note that you'll need to have the Android development environment set up on your computer, including the Android SDK and the Android platform tools, in order to use this command. You can follow the React Native documentation for instructions on setting up your development environment for Android.

Building the application for an Android device
================================

#. You can build the application using the command :code:`npx react-native run-android --variant=release`. This will build the :code:`.apk` file in the :code:`android\\app\\build\\outputs\\apk\\release\\` folder.
#. Share the :code:`.apk` file with your friends. They can easily install the application by downloading the file to their device and opening it there.

Running the application on an iOS device
================================

#. You can follow the `official documentation <https://reactnative.dev/docs/running-on-device>`_ for setting up the iOS environment.

Building the application for an iOS device
================================

#. Open your React Native project in Xcode.
#. Select the project in the Project navigator, and then select your app's target.
#. Under the *General* tab, change the *Bundle Identifier* to something unique (e.g., :code:`com.yourcompany.yourapp`).
#. Under the *Signing & Capabilities* tab, select a development team and make sure a valid provisioning profile is selected.
#. Select *Product* from the menu bar, and then select *Archive*.
#. Once the build is complete, select *Distribute App* and then select *Ad Hoc*.
#. Follow the prompts to export the :code:`IPA file`, which you can then transfer to your friend's iOS device using a file-sharing service like Dropbox or Google Drive.

Modifying the application
================================
* The main code of the application is located in the folder `src`. The file `App.tsx` is the backbone of the project. The rest of the components that will be called can be found in the other various folders. Feel free to add, remove, or modify these folders as necessary. **The only file that has a direct dependency on the rest of the project is the `App.tsx`**. 