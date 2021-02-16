---
UID: NS:wlanapi._WLAN_BSS_LIST
title: WLAN_BSS_LIST (wlanapi.h)
description: Contains a list of basic service set (BSS) entries.
helpviewer_keywords: ["*PWLAN_BSS_LIST","PWLAN_BSS_LIST","PWLAN_BSS_LIST structure pointer [NativeWIFI]","WLAN_BSS_LIST","WLAN_BSS_LIST structure [NativeWIFI]","nwifi.wlan_bss_list","wlanapi/PWLAN_BSS_LIST","wlanapi/WLAN_BSS_LIST"]
old-location: nwifi\wlan_bss_list.htm
tech.root: nwifi
ms.assetid: aeb68835-31ce-4fa7-980a-91a328fbcbc3
ms.date: 12/05/2018
ms.keywords: '*PWLAN_BSS_LIST, PWLAN_BSS_LIST, PWLAN_BSS_LIST structure pointer [NativeWIFI], WLAN_BSS_LIST, WLAN_BSS_LIST structure [NativeWIFI], nwifi.wlan_bss_list, wlanapi/PWLAN_BSS_LIST, wlanapi/WLAN_BSS_LIST'
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
req.typenames: WLAN_BSS_LIST, *PWLAN_BSS_LIST
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_BSS_LIST
 - wlanapi/_WLAN_BSS_LIST
 - PWLAN_BSS_LIST
 - wlanapi/PWLAN_BSS_LIST
 - WLAN_BSS_LIST
 - wlanapi/WLAN_BSS_LIST
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
 - WLAN_BSS_LIST
---

# WLAN_BSS_LIST structure


## -description

The <b>WLAN_BSS_LIST</b> structure contains a list of basic service set (BSS) entries.

## -struct-fields

### -field dwTotalSize

The total size of this structure, in bytes.

### -field dwNumberOfItems

The number of items in the <b>wlanBssEntries</b> member.

### -field wlanBssEntries

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a> structures that contains information about a BSS.

## -remarks

The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a> function retrieves the BSS list of the wireless network or networks on a given interface and returns this information in a <b>WLAN_BSS_LIST</b> structure. 



The <b>WLAN_BSS_LIST</b> structure may contain padding for alignment between the <b>dwTotalSize</b> member, the  <b>dwNumberOfItems</b> member, and the first <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a>  array entry in the <b>wlanBssEntries</b>  member. Padding for alignment may also be present between the <b>WLAN_BSS_ENTRY</b> array entries in the <b>wlanBssEntries</b> member. Any access to a <b>WLAN_BSS_ENTRY</b> array entry should assume padding may exist.


When the wireless LAN interface is also operating as  a Wireless Hosted Network , the BSS list will contain an entry for the BSS created for the Wireless Hosted Network.



Since the information is returned by the access point for an infrastructure BSS network or by the network peer for an independent BSS network (ad hoc network), the information returned should not be trusted. The <b>ulIeOffset</b> and <b>ulIeSize</b>  members in the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a> structure should be used to determine the maximum size of the information element data blob in the <b>WLAN_BSS_ENTRY</b> structure, not the data in the information element data blob.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a>