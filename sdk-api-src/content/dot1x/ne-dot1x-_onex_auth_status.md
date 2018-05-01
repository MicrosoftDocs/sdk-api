---
UID: NE:dot1x._ONEX_AUTH_STATUS
title: "_ONEX_AUTH_STATUS"
author: windows-driver-content
description: Specifies the possible values for the 802.1X authentication status.
old-location: nwifi\onex_auth_status.htm
old-project: NativeWiFi
ms.assetid: 9a5c7876-2c6b-450e-95e4-2766d63b6e19
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: ONEX_AUTH_STATUS, ONEX_AUTH_STATUS enumeration [NativeWIFI], OneXAuthFailure, OneXAuthInProgress, OneXAuthInvalid, OneXAuthNoAuthenticatorFound, OneXAuthNotStarted, OneXAuthSuccess, PONEX_AUTH_STATUS, PONEX_AUTH_STATUS enumeration pointer [NativeWIFI], _ONEX_AUTH_STATUS, dot1x/ONEX_AUTH_STATUS, dot1x/OneXAuthFailure, dot1x/OneXAuthInProgress, dot1x/OneXAuthInvalid, dot1x/OneXAuthNoAuthenticatorFound, dot1x/OneXAuthNotStarted, dot1x/OneXAuthSuccess, dot1x/PONEX_AUTH_STATUS, nwifi.onex_auth_status
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ONEX_AUTH_STATUS, PONEX_AUTH_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dot1x.h
api_name:
-	ONEX_AUTH_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

