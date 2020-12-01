---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
title: WLAN_HOSTED_NETWORK_PEER_AUTH_STATE (wlanapi.h)
description: Specifies the possible values for the authentication state of a peer on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE","PWLAN_HOSTED_NETWORK_PEER_STATE","PWLAN_HOSTED_NETWORK_PEER_STATE enumeration pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_PEER_AUTH_STATE","WLAN_HOSTED_NETWORK_PEER_AUTH_STATE enumeration [NativeWIFI]","nwifi.wlan_hosted_network_peer_auth_state","wlan_hosted_network_peer_state_authenticated","wlan_hosted_network_peer_state_invalid","wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE","wlanapi/WLAN_HOSTED_NETWORK_PEER_AUTH_STATE","wlanapi/wlan_hosted_network_peer_state_authenticated","wlanapi/wlan_hosted_network_peer_state_invalid"]
old-location: nwifi\wlan_hosted_network_peer_auth_state.htm
tech.root: nwifi
ms.assetid: 9953ad0c-eafc-49ad-b9a3-09fbfba805e5
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE, PWLAN_HOSTED_NETWORK_PEER_STATE enumeration pointer [NativeWIFI], WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, WLAN_HOSTED_NETWORK_PEER_AUTH_STATE enumeration [NativeWIFI], nwifi.wlan_hosted_network_peer_auth_state, wlan_hosted_network_peer_state_authenticated, wlan_hosted_network_peer_state_invalid, wlanapi/PWLAN_HOSTED_NETWORK_PEER_STATE, wlanapi/WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, wlanapi/wlan_hosted_network_peer_state_authenticated, wlanapi/wlan_hosted_network_peer_state_invalid'
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
req.typenames: WLAN_HOSTED_NETWORK_PEER_AUTH_STATE, *PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
 - wlanapi/_WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
 - PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE
 - wlanapi/PWLAN_HOSTED_NETWORK_PEER_AUTH_STATE
 - WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
 - wlanapi/WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
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
 - WLAN_HOSTED_NETWORK_PEER_AUTH_STATE
---

# WLAN_HOSTED_NETWORK_PEER_AUTH_STATE enumeration


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

<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change">WLAN_HOSTED_NETWORK_DATA_PEER_STATE_CHANGE</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_peer_state">WLAN_HOSTED_NETWORK_PEER_STATE</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>