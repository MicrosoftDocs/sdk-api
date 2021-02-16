---
UID: NS:wlanapi._DOT11_NETWORK_LIST
title: DOT11_NETWORK_LIST (wlanapi.h)
description: Contains a list of 802.11 wireless networks.
helpviewer_keywords: ["*PDOT11_NETWORK_LIST","DOT11_NETWORK_LIST","DOT11_NETWORK_LIST structure [NativeWIFI]","PDOT11_NETWORK_LIST","PDOT11_NETWORK_LIST structure pointer [NativeWIFI]","nwifi.dot11_network_list","wlanapi/DOT11_NETWORK_LIST","wlanapi/PDOT11_NETWORK_LIST"]
old-location: nwifi\dot11_network_list.htm
tech.root: nwifi
ms.assetid: 607c5795-8168-4c6b-a2f3-65f31aea5cf5
ms.date: 12/05/2018
ms.keywords: '*PDOT11_NETWORK_LIST, DOT11_NETWORK_LIST, DOT11_NETWORK_LIST structure [NativeWIFI], PDOT11_NETWORK_LIST, PDOT11_NETWORK_LIST structure pointer [NativeWIFI], nwifi.dot11_network_list, wlanapi/DOT11_NETWORK_LIST, wlanapi/PDOT11_NETWORK_LIST'
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: DOT11_NETWORK_LIST, *PDOT11_NETWORK_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOT11_NETWORK_LIST
 - wlanapi/_DOT11_NETWORK_LIST
 - PDOT11_NETWORK_LIST
 - wlanapi/PDOT11_NETWORK_LIST
 - DOT11_NETWORK_LIST
 - wlanapi/DOT11_NETWORK_LIST
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
 - DOT11_NETWORK_LIST
---

# DOT11_NETWORK_LIST structure


## -description

The <b>DOT11_NETWORK_LIST</b> structure contains a list of 802.11 wireless networks.

## -struct-fields

### -field dwNumberOfItems

Contains the number of items in the <b>Network</b> member.

### -field dwIndex

The index of the current item.  The index of the first item is 0. <b>dwIndex</b> must be less than <b>dwNumberOfItems</b>.

This member is not used by the wireless service. Applications can use this member when processing individual networks in the  <b>DOT11_NETWORK_LIST</b>  structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.

### -field Network.unique

### -field Network.size_is

### -field Network.size_is.dwNumberOfItems

### -field Network

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network">DOT11_NETWORK</a> structures that contain 802.11 wireless network information.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network">DOT11_NETWORK</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>