---
UID: NS:dot1x._ONEX_RESULT_UPDATE_DATA
title: "_ONEX_RESULT_UPDATE_DATA"
author: windows-driver-content
description: Contains information on a status change to 802.1X authentication.
old-location: nwifi\onex_result_update_data.htm
old-project: NativeWiFi
ms.assetid: 140386c8-2e35-4e83-812f-119bf8828d0b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PONEX_RESULT_UPDATE_DATA, ONEX_RESULT_UPDATE_DATA, ONEX_RESULT_UPDATE_DATA structure [NativeWIFI], PONEX_RESULT_UPDATE_DATA, PONEX_RESULT_UPDATE_DATA structure pointer [NativeWIFI], _ONEX_RESULT_UPDATE_DATA, dot1x/ONEX_RESULT_UPDATE_DATA, dot1x/PONEX_RESULT_UPDATE_DATA, nwifi.onex_result_update_data"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: ONEX_RESULT_UPDATE_DATA, *PONEX_RESULT_UPDATE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dot1x.h
api_name:
-	ONEX_RESULT_UPDATE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ONEX_RESULT_UPDATE_DATA structure


## -description


The <b>ONEX_RESULT_UPDATE_DATA</b> structure contains information on a status change to 802.1X authentication.


## -struct-fields




### -field oneXStatus

Specifies the current 802.1X authentication status. For more information, see the <a href="https://msdn.microsoft.com/2c19c65b-0943-4561-a28f-0104e1cbd229">ONEX_STATUS</a> structure.


### -field BackendSupport

Indicates if the configured EAP method on the supplicant is supported on the 802.1X authentication server.

EAP permits the use of a backend
   authentication server, which may implement some or all authentication
   methods, with the authenticator acting as a pass-through for some or
   all methods and peers. For more information, see RFC 3748 published by the IETF and the <a href="https://msdn.microsoft.com/ae0c30c3-331e-4b57-aa5f-f6b1f73dc69d">ONEX_EAP_METHOD_BACKEND_SUPPORT</a> enumeration.


### -field fBackendEngaged

Indicates if a response was received from the 802.1X authentication server.


### -field fOneXAuthParams

Indicates if the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains 802.1X authentication parameters in the <b>authParams</b> member.


### -field fEapError

Indicates if the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains an EAP error in the <b>eapError</b> member.


### -field authParams

The 802.1X authentication parameters. This member contains an embedded <a href="https://msdn.microsoft.com/a5dcd546-abe5-4553-baa8-656d37b263a3">ONEX_AUTH_PARAMS</a> structure starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fOneXAuthParams</b> bitfield member is set.


### -field eapError

An EAP error value. This member contains an embedded <a href="https://msdn.microsoft.com/20126b9a-732e-460d-bb10-4d7485b25eb9">ONEX_EAP_ERROR</a> structure starting at the <b>dwOffset</b> member of the <a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a> if the <b>fEapError</b> bitfield member is set.


## -remarks



The <b>ONEX_RESULT_UPDATE_DATA</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_RESULT_UPDATE_DATA</b> contains information on a status change to 802.1X authentication.This structure is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/a5dcd546-abe5-4553-baa8-656d37b263a3">ONEX_AUTH_PARAMS</a>



<a href="https://msdn.microsoft.com/20126b9a-732e-460d-bb10-4d7485b25eb9">ONEX_EAP_ERROR</a>



<a href="https://msdn.microsoft.com/ae0c30c3-331e-4b57-aa5f-f6b1f73dc69d">ONEX_EAP_METHOD_BACKEND_SUPPORT</a>



<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/2c19c65b-0943-4561-a28f-0104e1cbd229">ONEX_STATUS</a>



<a href="https://msdn.microsoft.com/3a410bde-bcff-4a86-aadc-650862dbf38b">ONEX_VARIABLE_BLOB</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

