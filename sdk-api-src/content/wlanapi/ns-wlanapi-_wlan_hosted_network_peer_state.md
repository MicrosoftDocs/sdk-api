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

# _WLAN_HOSTED_NETWORK_PEER_STATE structure


## -description


The <b>WLAN_HOSTED_NETWORK_PEER_STATE</b> structure contains information about the peer state for a peer on the wireless Hosted Network.


## -struct-fields




### -field PeerMacAddress

The MAC address of the peer being described.


### -field PeerAuthState

The current authentication state of this peer.


## -remarks



The <b>WLAN_HOSTED_NETWORK_PEER_STATE</b> structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548681">DOT11_MAC_ADDRESS</a>



<a href="https://msdn.microsoft.com/476b903d-7c87-4734-8a42-c8b75d292fb5">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a>



<a href="https://msdn.microsoft.com/9953ad0c-eafc-49ad-b9a3-09fbfba805e5">WLAN_HOSTED_NETWORK_PEER_AUTH_STATE</a>



<a href="https://msdn.microsoft.com/5fa00041-235f-4f48-a367-e1eaec8474ce">WLAN_HOSTED_NETWORK_STATUS</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>
 

 

