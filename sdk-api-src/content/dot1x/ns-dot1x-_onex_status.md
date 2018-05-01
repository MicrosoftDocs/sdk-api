---
UID: NS:dot1x._ONEX_STATUS
title: "_ONEX_STATUS"
author: windows-driver-content
description: Contains the current 802.1X authentication status.
old-location: nwifi\onex_status.htm
old-project: NativeWiFi
ms.assetid: 2c19c65b-0943-4561-a28f-0104e1cbd229
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PONEX_STATUS, ONEX_STATUS, ONEX_STATUS structure [NativeWIFI], PONEX_STATUS, PONEX_STATUS structure pointer [NativeWIFI], _ONEX_STATUS, dot1x/ONEX_STATUS, dot1x/PONEX_STATUS, nwifi.onex_status"
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
req.typenames: ONEX_STATUS, *PONEX_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dot1x.h
api_name:
-	ONEX_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ONEX_STATUS structure


## -description


The <b>ONEX_STATUS</b> structure contains the current 802.1X authentication status.


## -struct-fields




### -field authStatus

The current status of the 802.1X authentication process. Any error that may have occurred during authentication is indicated below by the value of the <b>dwReason</b> and <b>dwError</b> members of the <b>ONEX_STATUS</b> structure. For more information, see the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569845">ONEX_AUTH_STATUS</a> enumeration.


### -field dwReason

If an error occurred during 802.1X authentication, this member contains the reason for the error specified as a value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569846">ONEX_REASON_CODE</a> enumeration. This member is normally <b>ONEX_REASON_CODE_SUCCESS</b> 
 when 802.1X authentication is successful and no error occurs. 


### -field dwError

If an error occurred during 802.1X authentication, this member contains the error. This member is normally NO_ERROR, except when an EAPHost error occurs. 


## -remarks



The <b>ONEX_STATUS</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

The <b>oneXStatus</b> member of the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure contains an <b>ONEX_STATUS</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569846">ONEX_REASON_CODE</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

