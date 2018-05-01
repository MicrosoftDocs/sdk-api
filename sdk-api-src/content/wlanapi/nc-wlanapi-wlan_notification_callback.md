---
UID: NC:wlanapi.WLAN_NOTIFICATION_CALLBACK
title: WLAN_NOTIFICATION_CALLBACK
author: windows-driver-content
description: Defines the type of notification callback function.
old-location: nwifi\notif_callback.htm
old-project: NativeWiFi
ms.assetid: df721e77-3285-442b-aabd-2dccae85fda5
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: WLAN_NOTIFICATION_CALLBACK, WLAN_NOTIFICATION_CALLBACK function pointer [NativeWIFI], nwifi.notif_callback, wlanapi/WLAN_NOTIFICATION_CALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
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
req.typenames: WLX_TERMINAL_SERVICES_DATA, *PWLX_TERMINAL_SERVICES_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	wlanapi.h
api_name:
-	WLAN_NOTIFICATION_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WLAN_NOTIFICATION_CALLBACK callback


## -description


The <b>WLAN_NOTIFICATION_CALLBACK</b> callback function prototype defines the type of notification callback function.


## -parameters




### -param Arg1


### -param Arg2








#### - context

A pointer to the context information provided by the client when it registered for the notification.


#### - data

A pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure that contains the notification information.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the wlan_notification_acm_connection_complete and wlan_notification_acm_disconnected notifications are available.


## -returns



This function pointer does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <b>WLAN_NOTIFICATION_CALLBACK</b>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

Once registered, the callback function will be called whenever a notification is available until the client unregisters or closes the handle.

Any registration to receive notifications is automatically undone if the calling application closes its calling handle (by calling <a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) used to register for notifications with the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function  or if the process ends.


If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_ACM</b>, then the received notification is an auto configuration module notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <b>WLAN_NOTIFICATION_CALLBACK</b> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For more information on these notifications, see the <a href="https://msdn.microsoft.com/b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd">WLAN_NOTIFICATION_ACM</a> enumeration reference.

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_HNWK</b>, then the received notification is a wireless Hosted Network notification supported on Windows 7 and  on Windows Server 2008 R2 with the Wireless LAN Service installed. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <b>WLAN_NOTIFICATION_CALLBACK</b> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure. For more information on these notifications, see the <a href="https://msdn.microsoft.com/f01e4a42-3378-4ceb-b23b-5deb78fb18ca">WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</a> enumeration reference.

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_IHV</b>, then the received notification is an indepent hardware vendor (IHV) notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <b>WLAN_NOTIFICATION_CALLBACK</b> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure, which is specific to the IHV.  

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>, then the received notification is an 802.1X module notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <b>WLAN_NOTIFICATION_CALLBACK</b> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For more information on these notifications, see the <a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a> enumeration reference.

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_MSM</b>, then the received notification is a media specific module (MSM) notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <b>WLAN_NOTIFICATION_CALLBACK</b> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For more information on these notifications, see the <a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a> enumeration reference.

If the <b>NotificationSource</b> member of the  <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_SECURITY</b>, then the received notification is a security notification. No notifications are currently defined for <b>WLAN_NOTIFICATION_SOURCE_SECURITY</b>.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Notifications are handled by the Netman service. If the Netman service is disabled or unavailable, notifications will not be received. If a notification is not received within a reasonable period of time, an application should time out and query the current interface state.




## -see-also




<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/f01e4a42-3378-4ceb-b23b-5deb78fb18ca">WLAN_HOSTED_NETWORK_NOTIFICATION_CODE</a>



<a href="https://msdn.microsoft.com/b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd">WLAN_NOTIFICATION_ACM</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

