Every release of Firebase ANEs will work with specific versions of Dependency ANEs and Frameworks. This document will tell you what dependencies and frameworks should be used in your project if you are building your project using different versions of Firebase ANEs.

**Note1**: Always try to use the latest releases because we won't be able to provide support on older versions.  
**Note2**: Always try to use the latest AdobeAir SDK. Doing this will automatically solve a lot of weird error messages.  
**Note3**: Firebase ANEs will not run on simulators. make sure you are building on a real device.  
**Note4**: When updating the .framework files, always delete the old ones and then copy the new ones. Never overwrite them.  
**Note5**: Consider useing the [ANELAB](https://github.com/myflashlab/ANE-LAB/) software. It will automatically take care of ANEs installation.  

# V6.x.x #
Find the Android dependencies V12.0.1 on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/a9ac3e9fa2e9c002d99751246b1255e243fba1d5). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks V4.11.0 [from here](https://dl.google.com/firebase/sdk/ios/4_11_0/Firebase-4.11.0.zip). And finally, if you want to use Crashlytics, you should download the frameworks V3.10.1 [from here](https://storage.googleapis.com/firebase-preview-drop/ios/crashlytics/com.crashlytics.ios-manual.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V27.0.2 | overrideAir.ane V5.1.1
overrideAir.ane V5.1.1 | FirebaseAnalytics.framework
firebase_common.ane V12.0.1 | FirebaseCore.framework
firebase_iid.ane V12.0.1 | FirebaseCoreDiagnostics.framework
googlePlayServices_base.ane V12.0.1 | FirebaseNanoPB.framework
googlePlayServices_basement.ane V12.0.1 | FirebaseInstanceID.framework
googlePlayServices_tasks.ane V12.0.1 | GoogleToolboxForMac.framework
googlePlayServices_appinvite.ane V12.0.1 | nanopb.framework

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V6.x.x | firebaseCore.ane V6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_auth.ane V12.0.1 | FirebaseAuth.framework
. | GTMSessionFetcher.framework

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_database.ane V12.0.1 | FirebaseDatabase.framework
firebase_databaseConnection.ane V12.0.1 | leveldb-library.framework

**firebaseFirestore.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_firestore.ane V12.0.1 | BoringSSL.framework
. | FirebaseFirestore.framework
. | Protobuf.framework
. | gRPC.framework
. | gRPC-Core.framework
. | gRPC-ProtoRPC.framework
. | gRPC-RxLibrary.framework
. | leveldb-library.framework
. | **Resources:**  gRPCCertificates.bundle

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required for by Core
firebase_config.ane V12.0.1 | FirebaseRemoteConfig.framework
. | Protobuf.framework
. | FirebaseABTesting.framework

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required for by Core | +other frameworks/ANEs required by the Core
firebase_storage.ane V12.0.1 | FirebaseStorage.framework
firebase_storageCommon.ane V12.0.1 | GTMSessionFetcher.framework

**firebaseCrash.ane** *Deprecated, use Crashlytics instead.

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_crash.ane V12.0.1 | FirebaseCrash.framework
firebase_analyticsImpl.ane V12.0.1 | Protobuf.framework

**firebaseCrashlytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_analyticsImpl.ane V12.0.1 | [Crashlytics.framework V3.10.1](https://storage.googleapis.com/firebase-preview-drop/ios/crashlytics/com.crashlytics.ios-manual.zip)
. | [Fabric.framework V3.10.1](https://storage.googleapis.com/firebase-preview-drop/ios/crashlytics/com.crashlytics.ios-manual.zip)

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_messaging.ane V12.0.1 | FirebaseMessaging.framework
. | Protobuf.framework

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_analyticsImpl.ane V12.0.1 | 
firebase-analytics.ane V12.0.1 | 

**firebaseDynamicLinks.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_dynamicLinks.ane V12.0.1 | FirebaseDynamicLinks.framework
 
 **firebaseInvites.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane 6.x.x | firebaseCore.ane 6.x.x
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebaseDynamicLinks.ane V6.x.x | firebaseDynamicLinks.ane V6.x.x
+other ANEs required by the DynamicLinks | +other frameworks/ANEs required by the DynamicLinks
. | FirebaseInvites.framework
. | GTMOAuth2.framework
. | GTMSessionFetcher.framework
. | GoogleAPIClientForREST.framework
. | GoogleSignIn.framework
. | Protobuf.framework
. | **Resources:**  GINInviteResources.bundle, GoogleSignIn.bundle, GPPACLPickerResources.bundle


# V5.x.x #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/236eb77a96c17865de10f0eba0fed3db6e0909ed). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/4_0_3/Firebase-4.0.3.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V25.3.1 | overrideAir.ane V4.1.0
overrideAir.ane V4.1.0 | FirebaseAnalytics.framework
firebase_common.ane V11.0.2 | FirebaseCore.framework
firebase_iid.ane V11.0.2 | FirebaseCoreDiagnostics.framework
googlePlayServices_base.ane V11.0.2 | FirebaseNanoPB.framework
googlePlayServices_basement.ane V11.0.2 | FirebaseInstanceID.framework
googlePlayServices_tasks.ane V11.0.2 | GoogleToolboxForMac.framework
googlePlayServices_appinvite.ane V11.0.2 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_auth.ane V11.0.2 | FirebaseAuth.framework
. | GTMSessionFetcher.framework

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_database.ane V11.0.2 | FirebaseDatabase.framework
firebase_databaseConnection.ane V11.0.2 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required for by Core
firebase_config.ane V11.0.2 | FirebaseRemoteConfig.framework
. | Protobuf.framework

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required for by Core | +other frameworks/ANEs required by the Core
firebase_storage.ane V11.0.2 | FirebaseStorage.framework
firebase_storageCommon.ane V11.0.2 | GTMSessionFetcher.framework

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_crash.ane V11.0.2 | FirebaseCrash.framework
firebase_analyticsImpl.ane V11.0.2 | Protobuf.framework

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_messaging.ane V11.0.2 | FirebaseMessaging.framework
. | Protobuf.framework

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_analyticsImpl.ane V11.0.2 | 
firebase-analytics.ane V11.0.2 | 

**firebaseDynamicLinks.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_dynamicLinks.ane V11.0.2 | FirebaseDynamicLinks.framework
 
 **firebaseInvites.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V5.1.1 | firebaseCore.ane V5.1.1
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebaseDynamicLinks.ane V5.1.0 | firebaseDynamicLinks.ane V5.1.0
+other ANEs required by the DynamicLinks | +other frameworks/ANEs required by the DynamicLinks
. | FirebaseDynamicLinks.framework
. | FirebaseInvites.framework
. | GTMOAuth2.framework
. | GTMSessionFetcher.framework
. | GoogleAPIClientForREST.framework
. | GoogleSignIn.framework
. | Protobuf.framework

# V4.x.x #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/072a311ad98ec34f9a4c8078b1d2cdd4229a4aaa). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/3_13_0/Firebase-3.13.0.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V24.2.1 | overrideAir.ane V4.0.0
overrideAir.ane V4.0.0 | FirebaseAnalytics.framework V3.13.0
firebase_common.ane V10.2.0 | FirebaseCore.framework V3.13.0
firebase_iid.ane V10.2.0 | FirebaseInstanceID.framework V3.13.0
googlePlayServices_base.ane V10.2.0 | GoogleToolboxForMac.framework V3.13.0
googlePlayServices_basement.ane V10.2.0 | 
googlePlayServices_tasks.ane V10.2.0 | 
googlePlayServices_appinvite.ane V10.2.0 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_auth.ane V10.2.0 | FirebaseAuth.framework V3.13.0
. | GTMSessionFetcher.framework V3.13.0

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_database.ane V10.2.0 | FirebaseDatabase.framework V3.13.0
firebase_databaseConnection.ane V10.2.0 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required for by Core
firebase_config.ane V10.2.0 | FirebaseRemoteConfig.framework V3.13.0
. | Protobuf.framework V3.13.0

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required for by Core | +other frameworks/ANEs required by the Core
firebase_storage.ane V10.2.0 | FirebaseStorage.framework V3.13.0
firebase_storageCommon.ane V10.2.0 | GTMSessionFetcher.framework V3.13.0

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_crash.ane V10.2.0 | FirebaseCrash.framework V3.13.0
firebase_analyticsImpl.ane V10.2.0 | Protobuf.framework V3.13.0

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_messaging.ane V10.2.0 | FirebaseMessaging.framework V3.13.0
. | Protobuf.framework V3.13.0

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebase_analyticsImpl.ane V10.2.0 | 
firebase-analytics.ane V10.2.0 | 

**firebaseDynamicLinks.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
. | FirebaseDynamicLinks.framework V3.13.0
 
 **firebaseInvites.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V4.0.0 | firebaseCore.ane V4.0.0
+other ANEs required by the Core | +other frameworks/ANEs required by the Core
firebaseDynamicLinks.ane V4.0.0 | firebaseDynamicLinks.ane V4.0.0
+other ANEs required by the DynamicLinks | +other frameworks/ANEs required by the DynamicLinks
. | FirebaseDynamicLinks.framework V3.13.0
. | FirebaseInvites.framework V3.13.0
. | GTMOAuth2.framework V3.13.0
. | GTMSessionFetcher.framework V3.13.0
. | GoogleAPIClientForREST.framework V3.13.0
. | GoogleSignIn.framework V3.13.0
. | Protobuf.framework V3.13.0

# V3.x.x #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/3df030020e09c17f31603a492171ed2dc3d5aa7d). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/3_10_0/Firebase-3.10.0.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V24.2.1 | FirebaseAnalytics.framework V3.10.0
overrideAir.ane V3.0.0 | FirebaseCore.framework V3.10.0
firebase_common.ane V10.0.0 | FirebaseInstanceID.framework V3.10.0
firebase_iid.ane V10.0.0 | GoogleInterchangeUtilities.framework V3.10.0
googlePlayServices_base.ane V10.0.0 | GoogleSymbolUtilities.framework V3.10.0
googlePlayServices_basement.ane V10.0.0 | GoogleToolboxForMac.framework V3.10.0
googlePlayServices_tasks.ane V10.0.0 | 
googlePlayServices_appinvite.ane V10.0.0 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_auth.ane V10.0.0 | FirebaseAuth.framework V3.10.0
. | GTMSessionFetcher.framework V3.10.0

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_database.ane V10.0.0 | FirebaseDatabase.framework V3.10.0
firebase_databaseConnection.ane V10.0.0 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_config.ane V10.0.0 | FirebaseRemoteConfig.framework V3.10.0

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_storage.ane V10.0.0 | FirebaseStorage.framework V3.10.0
firebase_storageCommon.ane V10.0.0 | GTMSessionFetcher.framework V3.10.0

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_crash.ane V10.0.0 | FirebaseCrash.framework V3.10.0
firebase_analyticsImpl.ane V10.0.0 | 

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_messaging.ane V10.0.0 | FirebaseMessaging.framework V3.10.0

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_analyticsImpl.ane V10.0.0 | 
firebase-analytics.ane V10.0.0 | 

**firebaseDynamicLinks.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V3.0.0 | firebaseCore.ane V3.0.0
+other ANEs required by the Core | +other frameworks required by the Core
. | FirebaseDynamicLinks.framework V3.10.0

# V2.x.x #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/3df030020e09c17f31603a492171ed2dc3d5aa7d). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/3_10_0/Firebase-3.10.0.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V24.2.1 | FirebaseAnalytics.framework V3.10.0
overrideAir.ane V3.0.0 | FirebaseCore.framework V3.10.0
firebase_common.ane V10.0.0 | FirebaseInstanceID.framework V3.10.0
firebase_iid.ane V10.0.0 | GoogleInterchangeUtilities.framework V3.10.0
googlePlayServices_base.ane V10.0.0 | GoogleSymbolUtilities.framework V3.10.0
googlePlayServices_basement.ane V10.0.0 | GoogleToolboxForMac.framework V3.10.0
googlePlayServices_tasks.ane V10.0.0 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_auth.ane V10.0.0 | FirebaseAuth.framework V3.10.0
. | GTMSessionFetcher.framework V3.10.0

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_database.ane V10.0.0 | FirebaseDatabase.framework V3.10.0
firebase_databaseConnection.ane V10.0.0 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_config.ane V10.0.0 | FirebaseRemoteConfig.framework V3.10.0

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_storage.ane V10.0.0 | FirebaseStorage.framework V3.10.0
firebase_storageCommon.ane V10.0.0 | GTMSessionFetcher.framework V3.10.0

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_crash.ane V10.0.0 | FirebaseCrash.framework V3.10.0
firebase_analyticsImpl.ane V10.0.0 | 

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_messaging.ane V10.0.0 | FirebaseMessaging.framework V3.10.0

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V2.0.0 | firebaseCore.ane V2.0.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_analyticsImpl.ane V10.0.0 | 
firebase-analytics.ane V10.0.0 | 

# V1.2.0 #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/11eb0c7370b0a38da923e6f1adb77ba23a826e2b). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/3_6_0/Firebase.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V23.4.0 | FirebaseAnalytics.framework V3.6.0
firebase_common.ane V9.6.1 | FirebaseInstanceID.framework V3.6.0
firebase_iid.ane V9.6.1 | GoogleInterchangeUtilities.framework V3.6.0
googlePlayServices_base.ane V9.6.1 | GoogleSymbolUtilities.framework V3.6.0
googlePlayServices_basement.ane V9.6.1 | GoogleUtilities.framework V3.6.0
googlePlayServices_tasks.ane V9.6.1 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_auth.ane V9.6.1 | FirebaseAuth.framework V3.6.0
firebase_authCommon.ane V9.6.1 | GoogleNetworkingUtilities.framework V3.6.0
firebase_authModule.ane V9.6.1 | 

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_database.ane V9.6.1 | FirebaseDatabase.framework V3.6.0
firebase_databaseConnection.ane V9.6.1 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_config.ane V9.6.1 | FirebaseRemoteConfig.framework V3.6.0
. | GoogleIPhoneUtilities.framework V3.6.0

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_storage.ane V9.6.1 | FirebaseStorage.framework V3.6.0
firebase_storageCommon.ane V9.6.1 | GoogleNetworkingUtilities.framework V3.6.0

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_crash.ane V9.6.1 | FirebaseCrash.framework V3.6.0

**firebaseMessaging.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_messaging.ane V9.6.1 | FirebaseMessaging.framework V3.6.0
. | GoogleIPhoneUtilities.framework V3.6.0
 
**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.2.0 | firebaseCore.ane V1.2.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_analyticsImpl.ane V9.6.1 | 
firebase-analytics.ane V9.6.1 | 

----------------------------------------------------------

# V1.1.0 #
Find the Android dependencies on [this branch](https://github.com/myflashlab/common-dependencies-ANE/tree/d2e6ca60f511ca4baf219a67de57ebda90d56772). *The master branch may have newer versions of these files but if you are building for the specified version number, you will need this specific branch.* And download the iOS frameworks [from here](https://dl.google.com/firebase/sdk/ios/3_4_0/Firebase.zip).

**firebaseCore.ane**

On the Android side | On the iOS side
------------ | -------------
androidSupport.ane V23.4.0 | FirebaseAnalytics.framework V3.4.0
firebase_common.ane V9.4.0 | FirebaseInstanceID.framework V3.4.0
firebase_iid.ane V9.4.0 | GoogleInterchangeUtilities.framework V3.4.0
googlePlayServices_base.ane V9.4.0 | GoogleSymbolUtilities.framework V3.4.0
googlePlayServices_basement.ane V9.4.0 | GoogleUtilities.framework V3.4.0
googlePlayServices_tasks.ane V9.4.0 | 

**firebaseAuth.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_auth.ane V9.4.0 | FirebaseAuth.framework V3.4.0
firebase_authCommon.ane V9.4.0 | GoogleNetworkingUtilities.framework V3.4.0
firebase_authModule.ane V9.4.0 | GoogleParsingUtilities.framework V3.4.0

**firebaseDatabase.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_database.ane V9.4.0 | FirebaseDatabase.framework V3.4.0
firebase_databaseConnection.ane V9.4.0 | 

**firebaseRemoteConfig.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_config.ane V9.4.0 | FirebaseRemoteConfig.framework V3.4.0
. | GoogleIPhoneUtilities.framework V3.4.0

**firebaseAnalytics.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_analyticsImpl.ane V9.4.0 | 
firebase-analytics.ane V9.4.0 | 

**firebaseStorage.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_storage.ane V9.4.0 | FirebaseStorage.framework V3.4.0
firebase_storageCommon.ane V9.4.0 | GoogleSignIn.framework V3.4.0
. | GoogleAppUtilities.framework V3.4.0
. | GoogleAuthUtilities.framework V3.4.0
. | GoogleNetworkingUtilities.framework V3.4.0
. | GoogleSymbolUtilities.framework V3.4.0
. | GoogleUtilities.framework V3.4.0

**firebaseCrash.ane**

On the Android side | On the iOS side
------------ | -------------
firebaseCore.ane V1.1.0 | firebaseCore.ane V1.1.0
+other ANEs required by the Core | +other frameworks required by the Core
firebase_crash.ane V9.4.0 | FirebaseCrash.framework V3.4.0