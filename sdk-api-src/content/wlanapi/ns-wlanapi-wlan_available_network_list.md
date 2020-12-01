---
UID: NS:wlanapi._WLAN_AVAILABLE_NETWORK_LIST
title: WLAN_AVAILABLE_NETWORK_LIST (wlanapi.h)
description: Contains an array of information about available networks.
helpviewer_keywords: ["*PWLAN_AVAILABLE_NETWORK_LIST","PWLAN_AVAILABLE_NETWORK_LIST","PWLAN_AVAILABLE_NETWORK_LIST structure pointer [NativeWIFI]","WLAN_AVAILABLE_NETWORK_LIST","WLAN_AVAILABLE_NETWORK_LIST structure [NativeWIFI]","nwifi.wlan_available_network_list","nwifi.wlan_visible_network_list","wlanapi/PWLAN_AVAILABLE_NETWORK_LIST","wlanapi/WLAN_AVAILABLE_NETWORK_LIST"]
old-location: nwifi\wlan_available_network_list.htm
tech.root: nwifi
ms.assetid: 0ac508b2-9117-423d-89d3-982f070c70e2
ms.date: 12/05/2018
ms.keywords: '*PWLAN_AVAILABLE_NETWORK_LIST, PWLAN_AVAILABLE_NETWORK_LIST, PWLAN_AVAILABLE_NETWORK_LIST structure pointer [NativeWIFI], WLAN_AVAILABLE_NETWORK_LIST, WLAN_AVAILABLE_NETWORK_LIST structure [NativeWIFI], nwifi.wlan_available_network_list, nwifi.wlan_visible_network_list, wlanapi/PWLAN_AVAILABLE_NETWORK_LIST, wlanapi/WLAN_AVAILABLE_NETWORK_LIST'
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
req.typenames: WLAN_AVAILABLE_NETWORK_LIST, *PWLAN_AVAILABLE_NETWORK_LIST
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_AVAILABLE_NETWORK_LIST
 - wlanapi/_WLAN_AVAILABLE_NETWORK_LIST
 - PWLAN_AVAILABLE_NETWORK_LIST
 - wlanapi/PWLAN_AVAILABLE_NETWORK_LIST
 - WLAN_AVAILABLE_NETWORK_LIST
 - wlanapi/WLAN_AVAILABLE_NETWORK_LIST
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
 - WLAN_AVAILABLE_NETWORK_LIST
---

# WLAN_AVAILABLE_NETWORK_LIST structure


## -description

The <b>WLAN_AVAILABLE_NETWORK_LIST</b> structure contains an array of information about available networks.

## -struct-fields

### -field dwNumberOfItems

Contains the number of items in the <b>Network</b> member.

### -field dwIndex

The index of the current item.  The index of the first item is 0. <b>dwIndex</b> must be less than <b>dwNumberOfItems</b>.

This member is not used by the wireless service. Applications can use this member when processing individual networks in the   <b>WLAN_AVAILABLE_NETWORK_LIST</b>  structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.

### -field Network.unique

### -field Network.size_is

### -field Network.size_is.dwNumberOfItems

### -field Network

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a> structures containing interface information.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a>