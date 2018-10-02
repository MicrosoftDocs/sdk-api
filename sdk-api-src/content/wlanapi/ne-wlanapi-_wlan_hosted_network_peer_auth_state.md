---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
title: "_WLAN_HOSTED_NETWORK_PEER_AUTH_STATE"
author: windows-sdk-content
description: Specifies the possible values for the authentication state of a peer on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_peer_auth_state.htm
tech.root: NativeWiFi
ms.assetid: 9953ad0c-eafc-49ad-b9a3-09fbfba805e5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE enumeration pointer [NativeWIFI], WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, WLAN_HOSTED_NETWORK_PEER_AUTH_STATE enumeration [NativeWIFI], _WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, nwifi.wlan_hosted_network_peer_auth_state, wlan_hosted_network_peer_state_authenticated, wlan_hosted_network_peer_state_invalid, wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE, wlanapi/WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, wlanapi/wlan_hosted_network_peer_state_authenticated, wlanapi/wlan_hosted_network_peer_state_invalid"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
product: Windows
targetos: Windows
req.typenames: WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, *PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE
req.redist: 
---

# _WLAN_HOSTED_NETWORK_PEER_AUTH_STATE enumeration


## -description


The <b>WLAN_HOSTED_NETWORK_PEER_AUTH_STATE</b> enumerated type specifies the possible values for the authentication state of a peer on the wireless Hosted Network.


## -enum-fields




### -field wlan_hosted_network_peer_state_invalid

An invalid peer state.


### -field wlan_hosted_network_peer_state_authenticated

The peer is authenticated.


### -field v1_enum




## -remarks



The <b>WLAN_HOSTED_NETWORK_PEER_AUTH_STATE</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  




## -see-also




<a href="https://msdn.microsoft.com/476b903d-7c87-4734-8a42-c8b75d292fb5">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a>



<a href="https://msdn.microsoft.com/f42f7100-45c8-4dd3-ae01-07740cace871">WLAN_HOSTED_NETWORK_PEER_STATE</a>



<a href="https://msdn.microsoft.com/5fa00041-235f-4f48-a367-e1eaec8474ce">WLAN_HOSTED_NETWORK_STATUS</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>
 

 

