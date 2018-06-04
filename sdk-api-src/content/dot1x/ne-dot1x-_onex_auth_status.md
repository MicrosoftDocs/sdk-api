---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _ONEX_AUTH_STATUS enumeration


## -description


The <b>ONEX_AUTH_STATUS</b> enumerated type specifies the possible values for  the 802.1X authentication status.



## -enum-fields




### -field OneXAuthNotStarted

802.1X authentication was not started.


### -field OneXAuthInProgress

802.1X authentication is in progress.


### -field OneXAuthNoAuthenticatorFound

No 802.1X authenticator was found. The 802.1X authentication was attempted, but no 802.1X peer was found. In this case, either  the network does not support or is not configured to support the 802.1X standard. 


### -field OneXAuthSuccess

802.1X authentication was successful.


### -field OneXAuthFailure

802.1X authentication was a failure.


### -field OneXAuthInvalid

Indicates the end of the range that specifies the possible values for 802.1X authentication status.


## -remarks



The <b>ONEX_AUTH_STATUS</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_AUTH_STATUS</b> specifies the possible values for the 802.1X authentication status. A value from this enumeration is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notifications  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure that contains a <a href="https://msdn.microsoft.com/2c19c65b-0943-4561-a28f-0104e1cbd229">ONEX_STATUS</a>  structure member in the <b>oneXStatus</b> structure member. The <b>ONEX_STATUS</b>  structure contains a <b>ONEX_AUTH_STATUS</b> enumeration value in the <b>authStatus</b> member.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/2c19c65b-0943-4561-a28f-0104e1cbd229">ONEX_STATUS</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

