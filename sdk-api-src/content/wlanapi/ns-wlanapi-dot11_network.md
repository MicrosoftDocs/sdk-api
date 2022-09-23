---
UID: NS:wlanapi._DOT11_NETWORK
title: DOT11_NETWORK (wlanapi.h)
description: Contains information about an available wireless network. (DOT11_NETWORK)
helpviewer_keywords: ["*PDOT11_NETWORK","DOT11_NETWORK","DOT11_NETWORK structure [NativeWIFI]","PDOT11_NETWORK","PDOT11_NETWORK structure pointer [NativeWIFI]","nwifi.dot11_network","wlanapi/DOT11_NETWORK","wlanapi/PDOT11_NETWORK"]
old-location: nwifi\dot11_network.htm
tech.root: nwifi
ms.assetid: 95f58433-deef-4c47-8f6c-a9e7b0d52dad
ms.date: 12/05/2018
ms.keywords: '*PDOT11_NETWORK, DOT11_NETWORK, DOT11_NETWORK structure [NativeWIFI], PDOT11_NETWORK, PDOT11_NETWORK structure pointer [NativeWIFI], nwifi.dot11_network, wlanapi/DOT11_NETWORK, wlanapi/PDOT11_NETWORK'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DOT11_NETWORK, *PDOT11_NETWORK
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _DOT11_NETWORK
 - wlanapi/_DOT11_NETWORK
 - PDOT11_NETWORK
 - wlanapi/PDOT11_NETWORK
 - DOT11_NETWORK
 - wlanapi/DOT11_NETWORK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - DOT11_NETWORK
---

# DOT11_NETWORK structure


## -description

The <b>DOT11_NETWORK</b> structure contains information about an available wireless network.

## -struct-fields

### -field dot11Ssid

A <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that contains the SSID of a visible wireless network.

### -field dot11BssType

A <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> value that indicates the BSS type of the network.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a>
