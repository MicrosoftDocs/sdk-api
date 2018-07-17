---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_STATE_CHANGE
title: "_WLAN_HOSTED_NETWORK_STATE_CHANGE"
author: windows-sdk-content
description: Contains information about a network state change on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_state_change.htm
old-project: nativewifi
ms.assetid: e05607fd-da1e-49ae-b2eb-3ac4758df84c
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_STATE_CHANGE, PWLAN_HOSTED_NETWORK_STATE_CHANGE, PWLAN_HOSTED_NETWORK_STATE_CHANGE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_STATE_CHANGE, WLAN_HOSTED_NETWORK_STATE_CHANGE structure [NativeWIFI], _WLAN_HOSTED_NETWORK_STATE_CHANGE, nwifi.wlan_hosted_network_state_change, wlanapi/PWLAN_HOSTED_NETWORK_STATE_CHANGE, wlanapi/WLAN_HOSTED_NETWORK_STATE_CHANGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WLAN_HOSTED_NETWORK_STATE_CHANGE, *PWLAN_HOSTED_NETWORK_STATE_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_STATE_CHANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_HOSTED_NETWORK_STATE_CHANGE structure


## -description


The <b>WLAN_HOSTED_NETWORK_STATE_CHANGE</b> structure contains information about a network state change on the wireless Hosted Network.


## -struct-fields




### -field OldState

The previous network state on the wireless Hosted Network.


### -field NewState

The current network state on the wireless Hosted Network.


### -field StateChangeReason

The reason for the network state change.


## -remarks



The <b>WLAN_HOSTED_NETWORK_STATE_CHANGE</b> structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  




## -see-also




<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/4c845df3-6bc8-4e09-ac01-6c9180d43b16">WLAN_HOSTED_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

