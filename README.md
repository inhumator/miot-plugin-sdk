# MIOT SDK for React Native

**Please execute npm install before running**

**Please use the test package provided below to debug, do not use the online package to debug**

## Initialize

    1, Download the development environment, execute git clone git@github.com:MiEcosystem/miot-plugin-sdk.git

    2, Enter the root directory of the development environment from the command line, install node and npm, version 9.0+ ( **Recommended on mac: npm version 6.12.1, node version v12.13.1** )
       Built-in one-click installation development environment script
       Windows: Execute `bin/install_mihome_dev.bat` (please follow the prompts to turn off real-time security protection)
       MacOS: Execute `bin/install_mihome_dev.sh`

    3, Install the ReactNative base library, and execute npm install in the root directory

    ! Note that if you need to use a third-party library in your project (only for pure js implementation), please enter the project directory (such as projects/com.xiaomi.demo),
    Execute npm install --save xxxx, otherwise the package release will fail because the third-party library cannot be found

## Order

    Create project
    npm run create xxx.yyy.zzz
        Note: xxx.yyy.zzz is the project path name, and the project is located under projects/xxx.yyy.zzz after creation
    You can also use the template developed by Mijia
    npm run create xxx.xxx.xxx[plugin package name] -type empty : create an empty project
    npm run create xxx.xxx.xxx[plugin package name] -type common : Create a common template project (including: NavigationBar, CommonSetting, Multilingual, Privacy, Custom Scene, Firmware Upgrade)
    npm run create xxx.xxx.xxx[plugin package name] -type wifi : Create a wifi template project (including: general template function, device control and attribute subscription function)
    npm run create xxx.xxx.xxx[plugin package name] -type ble : Create a ble template project (including: general template functions, Bluetooth connection related functions)

    start debugging
    npm start xxx.yyy.zzz, use Mijia APP to scan the QR code in the console to start debugging.

    run demo
    Under /miot-workspace, execute
        npm install
    If fsevents reports an error under Windows, it can be ignored. Under mac, npm install fsevents@latest can be executed.
    For other errors, please check issues or submit a ticket. Then
        cd projects/com.xiaomi.demo
        npm install
    Then you can npm start and start debugging the demo

    **Note: The reason why you need to execute npm install again under com.xiaomi.demo is because we have introduced a pure js third-party library: react-native-root-toast in com.xiao.demo. Example introduced as a 3rd party library! If you don't execute npm install, directly debugging com.xiaomi.demo will report an error that react-native-root-toast cannot be found! **

    Publish the project
    npm run publish xxx.yyy.zzz
        Note: The default target file is located in projects/xxx.yyy.zzz/build/publish.mpkg, you can specify any target file by --target

## configure
After the project is created (such as xxx.yyy.zzz), there is a project configuration file project.json in the projects/xxx.yyy.zzz directory, the structure is as follows:

    {
        "package_path":"xxx.yyy.zzz", //Project path name
        "min_sdk_api_level":10000 //Supported SDK API_LEVEL
    }

## Notice

    1. It is not allowed to make any modification to the package.json file in the root directory, otherwise it will lead to failure of online packaging,
    2. Only allow third-party libraries to be referenced in their respective project directories (projects/xxx.yyy.zzz), modify the package.json below, and execute npm install
    3, It is not allowed to refer to any content of other projects under projects

## Documentation
🎉 UI component documentation officially released

[Official version](https://github.com/MiEcosystem/miot-plugin-sdk/blob/master/%E7%B1%B3%E5%AE%B6%E6%8F%92%E4%BB%B6%E9%80%9A%E7%94%A8UI%E7%BB%84%E4%BB%B6%E6%89%8B%E5%86%8C.md), including only released components

[Preview](https://github.com/MiEcosystem/miot-plugin-sdk/blob/ui_doc/%E7%B1%B3%E5%AE%B6%E6%8F%92%E4%BB%B6%E9%80%9A%E7%94%A8UI%E7%BB%84%E4%BB%B6%E6%89%8B%E5%86%8C.md), including the components that have been released and those that have been developed to be released components

For plugin development, please refer to ["MIOT SDK API"](https://github.com/MiEcosystem/miot-plugin-sdk/wiki)
            ["CHANGELOG"](https://github.com/MiEcosystem/miot-plugin-sdk/releases)

Please refer to ["Upgrade Guide"](https://github.com/MiEcosystem/miot-plugin-sdk/wiki/RN61%E5%BC%80%E5%8F%91%E8%80%85%E5%8D%87%E7%BA%A7%E6%8C%87%E5%8D%97)

For plugin migration from the old framework to the new framework, please refer to ["Migration Manual"](https://github.com/MiEcosystem/miot-plugin-sdk/blob/master/%E8%BF%81%E7%A7%BB%E6%89%8B%E5%86%8C.md)

For the plugin debugging process, please refer to ["Debugging Instructions"](https://github.com/MiEcosystem/miot-plugin-sdk/blob/master/%E8%B0%83%E8%AF%95%E8%AF%B4%E6%98%8E.md)


## Debug environment

iOS IPA package download QR code
![mihome](https://user-images.githubusercontent.com/6511522/159238473-fbf07ace-ef8d-442e-b299-7ffe6ea50f47.png)


Android APK package download address: http://d.maps9.com/MiHomeForAndroid

Download password: keliyuan


If the debugging package cannot be downloaded, please submit a work order.

## other documents

[Font usage](https://github.com/MiEcosystem/miot-plugin-sdk/blob/master/font.md)
