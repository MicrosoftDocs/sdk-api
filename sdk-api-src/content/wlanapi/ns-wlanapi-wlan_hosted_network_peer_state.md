---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_PEER_STATE
title: WLAN_HOSTED_NETWORK_PEER_STATE (wlanapi.h)
description: Contains information about the peer state for a peer on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_PEER_STATE","PWLAN_HOSTED_NETWORK_PEER_STATE","PWLAN_HOSTED_NETWORK_PEER_STATE structure pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_PEER_STATE","WLAN_HOSTED_NETWORK_PEER_STATE structure [NativeWIFI]","nwifi.wlan_hosted_network_peer_state","wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE","wlanapi/WLAN_HOSTED_NETWORK_PEER_STATE"]
old-location: nwifi\wlan_hosted_network_peer_state.htm
tech.root: nwifi
ms.assetid: f42f7100-45c8-4dd3-ae01-07740cace871
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_PEER_STATE, WLAN_HOSTED_NETWORK_PEER_STATE structure [NativeWIFI], nwifi.wlan_hosted_network_peer_state, wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE, wlanapi/WLAN_HOSTED_NETWORK_PEER_STATE'
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
targetos: Windows
req.typenames: WLAN_HOSTED_NETWORK_PEER_STATE, *PWLAN_HOSTED_NETWORK_PEER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_PEER_STATE
 - wlanapi/_WLAN_HOSTED_NETWORK_PEER_STATE
 - PWLAN_HOSTED_NETWORK_PEER_STATE
 - wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE
 - WLAN_HOSTED_NETWORK_PEER_STATE
 - wlanapi/WLAN_HOSTED_NETWORK_PEER_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_PEER_STATE
---

# WLAN_HOSTED_NETWORK_PEER_STATE structure


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

<a href="/windows/desktop/NativeWiFi/dot11-mac-address-type">DOT11_MAC_ADDRESS</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state">WLAN_HOSTED_NETWORK_PEER_AUTH_STATE</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>