---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_STATE
title: WLAN_HOSTED_NETWORK_STATE (wlanapi.h)
description: Specifies the possible values for the network state of the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_STATE","PWLAN_HOSTED_NETWORK_STATE","PWLAN_HOSTED_NETWORK_STATE enumeration [NativeWIFI]","WLAN_HOSTED_NETWORK_STATE","WLAN_HOSTED_NETWORK_STATE enumeration [NativeWIFI]","nwifi.wlan_hosted_network_state","wlan_hosted_network_active","wlan_hosted_network_idle","wlan_hosted_network_unavailable","wlanapi/PWLAN_HOSTED_NETWORK_STATE","wlanapi/WLAN_HOSTED_NETWORK_STATE","wlanapi/wlan_hosted_network_active","wlanapi/wlan_hosted_network_idle","wlanapi/wlan_hosted_network_unavailable"]
old-location: nwifi\wlan_hosted_network_state.htm
tech.root: nwifi
ms.assetid: 4c845df3-6bc8-4e09-ac01-6c9180d43b16
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_STATE, PWLAN_HOSTED_NETWORK_STATE, PWLAN_HOSTED_NETWORK_STATE enumeration [NativeWIFI], WLAN_HOSTED_NETWORK_STATE, WLAN_HOSTED_NETWORK_STATE enumeration [NativeWIFI], nwifi.wlan_hosted_network_state, wlan_hosted_network_active, wlan_hosted_network_idle, wlan_hosted_network_unavailable, wlanapi/PWLAN_HOSTED_NETWORK_STATE, wlanapi/WLAN_HOSTED_NETWORK_STATE, wlanapi/wlan_hosted_network_active, wlanapi/wlan_hosted_network_idle, wlanapi/wlan_hosted_network_unavailable'
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
req.typenames: WLAN_HOSTED_NETWORK_STATE, *PWLAN_HOSTED_NETWORK_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_STATE
 - wlanapi/_WLAN_HOSTED_NETWORK_STATE
 - PWLAN_HOSTED_NETWORK_STATE
 - wlanapi/PWLAN_HOSTED_NETWORK_STATE
 - WLAN_HOSTED_NETWORK_STATE
 - wlanapi/WLAN_HOSTED_NETWORK_STATE
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
 - WLAN_HOSTED_NETWORK_STATE
---

# WLAN_HOSTED_NETWORK_STATE enumeration


## -description

The <b>WLAN_HOSTED_NETWORK_STATE</b> enumerated type specifies the possible values for the network state of the wireless Hosted Network.

## -enum-fields

### -field wlan_hosted_network_unavailable

The wireless Hosted Network is unavailable.

### -field wlan_hosted_network_idle

The wireless Hosted Network is idle.

### -field wlan_hosted_network_active

The wireless Hosted Network is active.

### -field v1_enum

## -remarks

The <b>WLAN_HOSTED_NETWORK_STATE</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_state_change">WLAN_HOSTED_NETWORK_STATE_CHANGE</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a>