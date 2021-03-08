# Hacking Android AND IOS 
 ***
 - **Deeplinking**
 - **XSS**
# CHEAT SHEET

## AndroidManifest.xml

- Search tag "intent-filter"
- https://www.youtube.com/watch?v=f4E1S7M3e3o&ab_channel=BrandanJones
- Inside tag ** Activitity **

![Example intent-filter](images/1.png)

### CSRF via Deep Link
![CSRF- POC](images/2.png)

- https://www.apkmirror.com/apk/twitter-inc/periscope/periscope-1-25-5-93-release/periscope-live-video-1-25-5-93-3-android-apk-download/download/?forcebaseapk

![Command](images/3.png)
`
apktool d periscope_xx.apk
`
![Analyze manifest](images/4.png)

![Path Specific](images/5.png)

![POC](images/6.png)

### Use ADB
`
adb shell am start -a "android.intent.action.VIEW" -d "pscp://user/MKBHD"
`
### Use Drozer
-https://www.youtube.com/watch?v=RwM1sRMBDZM&ab_channel=BitsPlease

-https://www.youtube.com/watch?v=j2H-RnbUSsM&ab_channel=GeekCluster

`
run scanner.activity.browsable -a tv.periscope.android
`



### POC OUTSIDE
![POC](images/8.png)

## POC WEB

![](images/9.png)

## ATTACKING ANDROID VIEWS
![](images/10.png)
