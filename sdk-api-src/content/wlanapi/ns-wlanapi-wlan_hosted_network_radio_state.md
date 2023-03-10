---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_RADIO_STATE
title: WLAN_HOSTED_NETWORK_RADIO_STATE (wlanapi.h)
description: Contains information about the radio state on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_RADIO_STATE","PWLAN_HOSTED_NETWORK_RADIO_STATE","PWLAN_HOSTED_NETWORK_RADIO_STATE structure pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_RADIO_STATE","WLAN_HOSTED_NETWORK_RADIO_STATE structure [NativeWIFI]","nwifi.wlan_hosted_network_radio_state","wlanapi/PWLAN_HOSTED_NETWORK_RADIO_STATE","wlanapi/WLAN_HOSTED_NETWORK_RADIO_STATE"]
old-location: nwifi\wlan_hosted_network_radio_state.htm
tech.root: nwifi
ms.assetid: a84db78d-f6fd-48c4-80e8-a0d16f4dc3ed
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_RADIO_STATE, PWLAN_HOSTED_NETWORK_RADIO_STATE, PWLAN_HOSTED_NETWORK_RADIO_STATE structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_RADIO_STATE, WLAN_HOSTED_NETWORK_RADIO_STATE structure [NativeWIFI], nwifi.wlan_hosted_network_radio_state, wlanapi/PWLAN_HOSTED_NETWORK_RADIO_STATE, wlanapi/WLAN_HOSTED_NETWORK_RADIO_STATE'
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
req.typenames: WLAN_HOSTED_NETWORK_RADIO_STATE, *PWLAN_HOSTED_NETWORK_RADIO_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_RADIO_STATE
 - wlanapi/_WLAN_HOSTED_NETWORK_RADIO_STATE
 - PWLAN_HOSTED_NETWORK_RADIO_STATE
 - wlanapi/PWLAN_HOSTED_NETWORK_RADIO_STATE
 - WLAN_HOSTED_NETWORK_RADIO_STATE
 - wlanapi/WLAN_HOSTED_NETWORK_RADIO_STATE
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
 - WLAN_HOSTED_NETWORK_RADIO_STATE
---

# WLAN_HOSTED_NETWORK_RADIO_STATE structure


## -description

The <b>WLAN_HOSTED_NETWORK_RADIO_STATE</b> structure contains information about the radio state on the wireless Hosted Network.

## -struct-fields

### -field dot11SoftwareRadioState

The software radio state of the wireless Hosted Network.

### -field dot11HardwareRadioState

The hardware radio state of the wireless Hosted Network.

## -remarks

The <b>WLAN_HOSTED_NETWORK_RADIO_STATE</b> structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.

## -see-also

<a href="/windows/win32/api/wlanapi/ne-wlanapi-dot11_radio_state-r1">DOT11_RADIO_STATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>