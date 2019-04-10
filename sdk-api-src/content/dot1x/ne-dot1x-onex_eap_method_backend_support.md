---
UID: NE:dot1x._ONEX_EAP_METHOD_BACKEND_SUPPORT
title: ONEX_EAP_METHOD_BACKEND_SUPPORT (dot1x.h)
author: windows-sdk-content
description: Specifies the possible values for whether the EAP method configured on the supplicant for 802.1X authentication is supported on the authentication server.
old-location: nwifi\onex_eap_method_backend_support.htm
tech.root: NativeWiFi
ms.assetid: ae0c30c3-331e-4b57-aa5f-f6b1f73dc69d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ONEX_EAP_METHOD_BACKEND_SUPPORT, ONEX_EAP_METHOD_BACKEND_SUPPORT enumeration [NativeWIFI], OneXEapMethodBackendSupportUnknown, OneXEapMethodBackendSupported, OneXEapMethodBackendUnsupported, dot1x/ONEX_EAP_METHOD_BACKEND_SUPPORT, dot1x/OneXEapMethodBackendSupportUnknown, dot1x/OneXEapMethodBackendSupported, dot1x/OneXEapMethodBackendUnsupported, nwifi.onex_eap_method_backend_support
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dot1x.h
api_name:
 - ONEX_EAP_METHOD_BACKEND_SUPPORT
product: Windows
targetos: Windows
req.typenames: ONEX_EAP_METHOD_BACKEND_SUPPORT
req.redist: 
---

# ONEX_EAP_METHOD_BACKEND_SUPPORT enumeration


## -description


The <b>ONEX_EAP_METHOD_BACKEND_SUPPORT</b> enumerated type specifies the possible values for  whether the EAP method configured on the supplicant for 802.1X authentication is supported on the authentication server.



## -enum-fields




### -field OneXEapMethodBackendSupportUnknown

It is not known whether the EAP method configured on the supplicant for 802.1X authentication is supported on the authentication server. This value can be returned if the 802.1X authentication process is in the initial state.


### -field OneXEapMethodBackendSupported

The EAP method configured on the supplicant for 802.1X authentication is supported on the authentication server. The 802.1X handshake is used to decide what is an acceptable EAP method to use.


### -field OneXEapMethodBackendUnsupported

The EAP method configured on the supplicant for 802.1X authentication is not supported on the authentication server. 


## -remarks



The <b>ONEX_EAP_METHOD_BACKEND_SUPPORT</b> enumeration is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

The <b>BackendSupport</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> struct contains a value from the <b>ONEX_EAP_METHOD_BACKEND_SUPPORT</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

