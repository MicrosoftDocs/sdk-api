---
UID: NS:dot1x._ONEX_VARIABLE_BLOB
title: "_ONEX_VARIABLE_BLOB"
author: windows-driver-content
description: Is used as a member of other 802.1X authentication stuctures to contain variable-sized members.
old-location: nwifi\onex_variable_blob.htm
old-project: NativeWiFi
ms.assetid: 3a410bde-bcff-4a86-aadc-650862dbf38b
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PONEX_VARIABLE_BLOB, ONEX_VARIABLE_BLOB, ONEX_VARIABLE_BLOB structure [NativeWIFI], PONEX_VARIABLE_BLOB, PONEX_VARIABLE_BLOB structure pointer [NativeWIFI], _ONEX_VARIABLE_BLOB, dot1x/ONEX_VARIABLE_BLOB, dot1x/PONEX_VARIABLE_BLOB, nwifi.onex_variable_blob"
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
req.typenames: ONEX_VARIABLE_BLOB, *PONEX_VARIABLE_BLOB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dot1x.h
api_name:
-	ONEX_VARIABLE_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ONEX_VARIABLE_BLOB structure


## -description


The <b>ONEX_VARIABLE_BLOB</b> structure is used as a member of other 802.1X authentication stuctures to contain variable-sized members..


## -struct-fields




### -field dwSize

The size, in bytes, of this <b>ONEX_VARIABLE_BLOB</b> structure.


### -field dwOffset

The offset, in bytes, from the beginning of the containing outer structure (where the <b>ONEX_VARIABLE_BLOB</b> structure is a  member) to the data contained in the <b>ONEX_VARIABLE_BLOB</b> structure.


## -remarks



The <b>ONEX_VARIABLE_BLOB</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

A number of the nested structure members in the <a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a> structure contains members of the <b>ONEX_VARIABLE_BLOB</b> type.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/a5dcd546-abe5-4553-baa8-656d37b263a3">ONEX_AUTH_PARAMS</a>



<a href="https://msdn.microsoft.com/20126b9a-732e-460d-bb10-4d7485b25eb9">ONEX_EAP_ERROR</a>



<a href="https://msdn.microsoft.com/c5892938-9798-4c09-a766-4924cda4d090">ONEX_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/140386c8-2e35-4e83-812f-119bf8828d0b">ONEX_RESULT_UPDATE_DATA</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

