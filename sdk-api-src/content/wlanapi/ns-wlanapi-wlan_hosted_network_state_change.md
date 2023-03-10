---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_STATE_CHANGE
title: WLAN_HOSTED_NETWORK_STATE_CHANGE (wlanapi.h)
description: Contains information about a network state change on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_STATE_CHANGE","PWLAN_HOSTED_NETWORK_STATE_CHANGE","PWLAN_HOSTED_NETWORK_STATE_CHANGE structure pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_STATE_CHANGE","WLAN_HOSTED_NETWORK_STATE_CHANGE structure [NativeWIFI]","nwifi.wlan_hosted_network_state_change","wlanapi/PWLAN_HOSTED_NETWORK_STATE_CHANGE","wlanapi/WLAN_HOSTED_NETWORK_STATE_CHANGE"]
old-location: nwifi\wlan_hosted_network_state_change.htm
tech.root: nwifi
ms.assetid: e05607fd-da1e-49ae-b2eb-3ac4758df84c
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_STATE_CHANGE, PWLAN_HOSTED_NETWORK_STATE_CHANGE, PWLAN_HOSTED_NETWORK_STATE_CHANGE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_STATE_CHANGE, WLAN_HOSTED_NETWORK_STATE_CHANGE structure [NativeWIFI], nwifi.wlan_hosted_network_state_change, wlanapi/PWLAN_HOSTED_NETWORK_STATE_CHANGE, wlanapi/WLAN_HOSTED_NETWORK_STATE_CHANGE'
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
req.typenames: WLAN_HOSTED_NETWORK_STATE_CHANGE, *PWLAN_HOSTED_NETWORK_STATE_CHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_STATE_CHANGE
 - wlanapi/_WLAN_HOSTED_NETWORK_STATE_CHANGE
 - PWLAN_HOSTED_NETWORK_STATE_CHANGE
 - wlanapi/PWLAN_HOSTED_NETWORK_STATE_CHANGE
 - WLAN_HOSTED_NETWORK_STATE_CHANGE
 - wlanapi/WLAN_HOSTED_NETWORK_STATE_CHANGE
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
 - WLAN_HOSTED_NETWORK_STATE_CHANGE
---

# WLAN_HOSTED_NETWORK_STATE_CHANGE structure


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

<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_state">WLAN_HOSTED_NETWORK_STATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>