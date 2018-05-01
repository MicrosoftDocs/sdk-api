---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_PEER_STATE
title: "_WLAN_HOSTED_NETWORK_PEER_STATE"
author: windows-driver-content
description: Contains information about the peer state for a peer on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_peer_state.htm
old-project: NativeWiFi
ms.assetid: f42f7100-45c8-4dd3-ae01-07740cace871
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_PEER_STATE, WLAN_HOSTED_NETWORK_PEER_STATE structure [NativeWIFI], _WLAN_HOSTED_NETWORK_PEER_STATE, nwifi.wlan_hosted_network_peer_state, wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE, wlanapi/WLAN_HOSTED_NETWORK_PEER_STATE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WLAN_HOSTED_NETWORK_PEER_STATE, *PWLAN_HOSTED_NETWORK_PEER_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wlanapi.h
api_name:
-	WLAN_HOSTED_NETWORK_PEER_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

