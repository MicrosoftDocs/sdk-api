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

# _ONEX_AUTH_RESTART_REASON enumeration


## -description


The <b>ONEX_AUTH_RESTART_REASON</b> enumerated type specifies the possible reasons that 802.1X authentication was restarted.



## -enum-fields




### -field OneXRestartReasonPeerInitiated

The EAPHost component (the peer) requested the 802.1x module to restart 802.1X authentication. This results from a <a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a> function call that returns an <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseAction</a> enumeration value of <b>EapHostPeerResponseStartAuthentication</b> in the <i>pEapOutput</i> parameter. 


### -field OneXRestartReasonMsmInitiated

The Media Specific Module (MSM) initiated the 802.1X authentication restart.


### -field OneXRestartReasonOneXHeldStateTimeout

The 802.1X authentication restart was the result of a state timeout. The timer expiring is the heldWhile timer of the 802.1X supplicant state machine defined in IEEE 802.1X - 2004 standard for Port-Based Network Access Control. The heldWhile timer is used by the supplicant state machine to define periods of time during which it
will not attempt to acquire an authenticator.


### -field OneXRestartReasonOneXAuthTimeout

The 802.1X authentication restart was the result of an state timeout. The timer expiring is the authWhile timer of the 802.1X supplicant port access entity defined in IEEE 802.1X - 2004 standard for Port-Based Network Access Control. The authWhile timer is used by the supplicant port access entity to determine how long to wait for a request from
the authenticator before timing it out.


### -field OneXRestartReasonOneXConfigurationChanged

The 802.1X authentication restart was the result of a configuration change to the current profile.


### -field OneXRestartReasonOneXUserChanged

The 802.1X authentication restart was the result of a change of user. This could occur if the current user logs off and new user logs on to the local computer.


### -field OneXRestartReasonQuarantineStateChanged

The 802.1X authentication restart was the result of receiving a notification from the EAP quarantine enforcement client (QEC) due to a network health change. If an EAPHost supplicant is participating in network access protection (NAP), the supplicant will respond to changes in the state of its network health. If that state changes, the supplicant must then initiate a re-authentication session. For more information, see the <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a> function. 


### -field OneXRestartReasonAltCredsTrial

The 802.1X authentication restart was caused by a new authentication attempt with alternate user credentials. EAP methods like MSCHAPv2 prefer to use logged-on user credentials for 802.1X authentication. If these user credentials do not work, then a dialog will be displayed to the user that asks permission to use alternate credentials for 802.1X authentication. For more information, see the <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a> function and EAP_FLAG_PREFER_ALT_CREDENTIALS flag in the <i>dwflags</i> parameter. 


### -field OneXRestartReasonInvalid

Indicates the end of the range that specifies the possible reasons that 802.1X authentication was restarted.


## -remarks



The <b>ONEX_AUTH_RESTART_REASON</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_AUTH_RESTART_REASON</b> specifies the possible values for the reason that 802.1X authentication was restarted. A value from this enumeration is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notifications  is <b>OneXNotificationTypeAuthRestarted</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_AUTH_RESTART_REASON</b> enumeration value that identifies the reason the authentication was restarted.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>



<a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a>



<a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseAction</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

