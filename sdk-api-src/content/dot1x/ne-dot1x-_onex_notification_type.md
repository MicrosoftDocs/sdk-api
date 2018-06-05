---
UID: NE:dot1x._ONEX_NOTIFICATION_TYPE
title: "_ONEX_NOTIFICATION_TYPE"
author: windows-sdk-content
description: Specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure for 802.1X module notifications.
old-location: nwifi\onex_notification_type.htm
old-project: NativeWiFi
ms.assetid: c5892938-9798-4c09-a766-4924cda4d090
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: ONEX_NOTIFICATION_TYPE, ONEX_NOTIFICATION_TYPE enumeration [NativeWIFI], OneXNotificationTypeAuthRestarted, OneXNotificationTypeEventInvalid, OneXNotificationTypeResultUpdate, OneXNumNotifications, OneXPublicNotificationBase, PONEX_NOTIFICATION_TYPE, PONEX_NOTIFICATION_TYPE enumeration pointer [NativeWIFI], _ONEX_NOTIFICATION_TYPE, dot1x/ONEX_NOTIFICATION_TYPE, dot1x/OneXNotificationTypeAuthRestarted, dot1x/OneXNotificationTypeEventInvalid, dot1x/OneXNotificationTypeResultUpdate, dot1x/OneXNumNotifications, dot1x/OneXPublicNotificationBase, dot1x/PONEX_NOTIFICATION_TYPE, nwifi.onex_notification_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dot1x.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ONEX_NOTIFICATION_TYPE, PONEX_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dot1x.h
api_name:
-	ONEX_NOTIFICATION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ONEX_NOTIFICATION_TYPE enumeration


## -description


The <b>ONEX_NOTIFICATION_TYPE</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for 802.1X module notifications.


## -enum-fields




### -field OneXPublicNotificationBase

Indicates the beginning of the range that specifies the possible values for 802.1X notifications.


### -field OneXNotificationTypeResultUpdate

Indicates that 802.1X authentication has a status change.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure that contains 802.1X update data. 


### -field OneXNotificationTypeAuthRestarted

Indicates that 802.1X authentication restarted.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to an  <a href="https://msdn.microsoft.com/794231da-ef4e-4419-9ff8-9b23483853d1">ONEX_AUTH_RESTART_REASON</a> enumeration value that identifies the reason the authentication was restarted.


### -field OneXNotificationTypeEventInvalid

Indicates the end of the range that specifies the possible values for 802.1X notifications.


### -field OneXNumNotifications

Indicates the end of the range that specifies the possible values for 802.1X notifications.


## -remarks



The <b>ONEX_NOTIFICATION_TYPE</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_NOTIFICATION_TYPE</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>. 

The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/794231da-ef4e-4419-9ff8-9b23483853d1">ONEX_AUTH_RESTART_REASON</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

