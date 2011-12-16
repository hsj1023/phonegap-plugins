# Install

* Copy the sample AppDelegate.h/m files from the sample into your project (they replace the autogenerated files)
* Include PushNotification.js in your WWW folder
* Add PushNotification.h/m in the Plugins folder
* Add key "pushnotification" and value "PushNotification" (case-sensitive) to the plugins list in PhoneGap.plist
* Include the sample index.html or just use the parts you want

# Provisioning profiles and XCode4

When trying to get this plugin setup I would receive an error: "no valid 'aps-environment' entitlement string found for application". To fix it I had to do the following:

* Delete old provisioning profiles from both Library + Device panels in Organizer
* Regenerate new profile with APN dev enabled from the developer portal website
* Make sure new profile is added to both Library + Device panels in Organizer
* Manually delete my app off my device (holding till it jiggles and hitting X)
* CMD+OPT+SHIFT+K (Clean Build Folder) and CMD+SHIFT+K (Clean)
* Set the proper profile under Targets > Build Settings > Code Signing
* Make sure 'Use Entitlements' is not checked under Targets > Summary

# Notes

This was forked from the now unmaintained https://github.com/urbanairship/ios-phonegap-plugin with the endorsement of the UA engineering team