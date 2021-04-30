---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
title: WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS (wlanapi.h)
description: Contains information about the connection settings on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS","PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS","PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS structure pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS","WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS structure [NativeWIFI]","nwifi.wlan_hosted_network_connection_settings","wlanapi/PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS","wlanapi/WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS"]
old-location: nwifi\wlan_hosted_network_connection_settings.htm
tech.root: nwifi
ms.assetid: 845eaef2-7ce0-4d7a-8273-8b843b5c95fd
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS, PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS, PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS, WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS structure [NativeWIFI], nwifi.wlan_hosted_network_connection_settings, wlanapi/PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS, wlanapi/WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS'
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
req.typenames: WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS, *PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
 - wlanapi/_WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
 - PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
 - wlanapi/PWLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
 - WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
 - wlanapi/WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
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
 - WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS
---

# WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS structure


## -description

The <b>WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</b> structure contains information about the connection settings on the wireless Hosted Network.

## -struct-fields

### -field hostedNetworkSSID

The SSID associated with the wireless Hosted Network.

### -field dwMaxNumberOfPeers

The maximum number of concurrent peers allowed by the wireless Hosted Network.

## -remarks

The <b>WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</b> structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.

## -see-also

<a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>