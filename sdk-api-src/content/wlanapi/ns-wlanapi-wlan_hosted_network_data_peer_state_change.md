---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE
title: WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE (wlanapi.h)
author: windows-sdk-content
description: Contains information about a network state change for a data peer on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_data_peer_state_change.htm
tech.root: NativeWiFi
ms.assetid: 476b903d-7c87-4734-8a42-c8b75d292fb5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE, PWLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE, PWLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE, WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE structure [NativeWIFI], nwifi.wlan_hosted_network_data_peer_state_change, wlanapi/PWLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE, wlanapi/WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE
product: Windows
targetos: Windows
req.typenames: WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE, *PWLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE
req.redist: 
---

# WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE structure


## -description


The <b>WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</b> structure contains information about a network state change for a data peer on the wireless Hosted Network.


## -struct-fields




### -field OldState

The previous network state for a data peer on the wireless Hosted Network.


### -field NewState

The current network state for a data peer on the wireless Hosted Network.

The reason for the network state change for the data peer.


### -field PeerStateChangeReason

 




## -remarks



The <b>WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</b> structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  




## -see-also




<a href="https://msdn.microsoft.com/f42f7100-45c8-4dd3-ae01-07740cace871">WLAN_HOSTED_NETWORK_PEER_STATE</a>



<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>
 

 

