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

# _ONEX_AUTH_PARAMS structure


## -description


The <b>ONEX_AUTH_PARAMS</b> structure contains 802.1X authentication parameters used for 802.1X authentication.


## -struct-fields




### -field fUpdatePending

Indicates if a status update is pending for 802.X authentication.


### -field oneXConnProfile

The 802.1X authentication connection profile. This member contains an embedded <a href="https://msdn.microsoft.com/ec494c74-bc79-445a-8889-a6f441e95ac5">ONEX_CONNECTION_PROFILE</a> structure starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a>. 


### -field authIdentity

The identity used for 802.1X authentication status. This member is a value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569844">ONEX_AUTH_IDENTITY</a> enumeration.


### -field dwQuarantineState

The quarantine isolation state value of the local computer. The isolation state determines its network connectivity. This member corresponds to a value from the EAPHost <a href="https://msdn.microsoft.com/460e447b-87c6-41df-8e8b-055e95426ca6">ISOLATION_STATE</a> enumeration.


### -field fSessionId

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a session ID in the <b>dwSessionId</b> member.


### -field fhUserToken

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a user token handle in the <b>hUserToken</b> member. 

For security reasons, the <b>hUserToken</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.  


### -field fOnexUserProfile

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains an 802.1X user profile in the <b>OneXUserProfile</b> member.

For security reasons, the <b>OneXUserProfile</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.  


### -field fIdentity

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains an 802.1X identity in the <b>Identity</b> member.


### -field fUserName

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a user name used for 802.1X authentication in the <b>UserName</b> member.


### -field fDomain

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a domain used for 802.1X authentication in the <b>Domain</b> member.


### -field dwSessionId

The session ID of the user currently logged on to the console. This member corresponds to the value returned by the <a href="https://msdn.microsoft.com/9aa43cfa-9518-428b-95a1-004fa23df90b">WTSGetActiveConsoleSessionId</a> function. This member contains a session ID if the <b>fSessionId</b> bitfield member is set.


### -field hUserToken

The user token handle  used for 802.1X authentication. This member contains a user token handle if the <b>fhUserToken</b> bitfield member is set.

For security reasons, the <b>hUserToken</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.  


### -field OneXUserProfile

The 802.1X user profile used for 802.1X authentication. This member contains an embedded user profile starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fOneXUserProfile</b> bitfield member is set. 

For security reasons, the <b>OneXUserProfile</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.  


### -field Identity

The 802.1X identity used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the identity starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fIdentity</b> bitfield member is set.


### -field UserName

The user name used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the user name starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fUserName</b> bitfield member is set.


### -field Domain

The domain used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the domain starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fDomain</b> bitfield member is set.


## -remarks



The <b>ONEX_AUTH_PARAMS</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

If the <b>fOneXAuthParams</b> member in the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure is set, then the  <b>authParams</b> member of the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains an <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> structure with an <b>ONEX_AUTH_PARAMS</b> structure embedded starting at the <b>dwOffset</b> member of the  <b>ONEX_VARIABLE_BLOB</b>.

For security reasons, the <b>hUserToken</b> and <b>OneXUserProfile</b> members of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member are always set to <b>NULL</b>.  




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/460e447b-87c6-41df-8e8b-055e95426ca6">ISOLATION_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569844">ONEX_AUTH_IDENTITY</a>



<b>ONEX_EAP_ERROR</b>



<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/9aa43cfa-9518-428b-95a1-004fa23df90b">WTSGetActiveConsoleSessionId</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

