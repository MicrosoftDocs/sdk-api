---
UID: NS:wlanapi._WLAN_BSS_LIST
title: "_WLAN_BSS_LIST"
author: windows-sdk-content
description: Contains a list of basic service set (BSS) entries.
old-location: nwifi\wlan_bss_list.htm
tech.root: nativewifi
ms.assetid: aeb68835-31ce-4fa7-980a-91a328fbcbc3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWLAN_BSS_LIST, PWLAN_BSS_LIST, PWLAN_BSS_LIST structure pointer [NativeWIFI], WLAN_BSS_LIST, WLAN_BSS_LIST structure [NativeWIFI], _WLAN_BSS_LIST, nwifi.wlan_bss_list, wlanapi/PWLAN_BSS_LIST, wlanapi/WLAN_BSS_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_BSS_LIST
product: Windows
targetos: Windows
req.typenames: WLAN_BSS_LIST, *PWLAN_BSS_LIST
req.redist: Wireless LAN API for Windows XP with SP2
---

# _WLAN_BSS_LIST structure


## -description


The <b>WLAN_BSS_LIST</b> structure contains a list of basic service set (BSS) entries.


## -struct-fields




### -field dwTotalSize

The total size of this structure, in bytes.


### -field dwNumberOfItems

The number of items in the <b>wlanBssEntries</b> member.


### -field wlanBssEntries

An array of <a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a> structures that contains information about a BSS.


## -remarks



The <a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a> function retrieves the BSS list of the wireless network or networks on a given interface and returns this information in a <b>WLAN_BSS_LIST</b> structure. 



The <b>WLAN_BSS_LIST</b> structure may contain padding for alignment between the <b>dwTotalSize</b> member, the  <b>dwNumberOfItems</b> member, and the first <a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a>  array entry in the <b>wlanBssEntries</b>  member. Padding for alignment may also be present between the <b>WLAN_BSS_ENTRY</b> array entries in the <b>wlanBssEntries</b> member. Any access to a <b>WLAN_BSS_ENTRY</b> array entry should assume padding may exist.


When the wireless LAN interface is also operating as  a Wireless Hosted Network , the BSS list will contain an entry for the BSS created for the Wireless Hosted Network.



Since the information is returned by the access point for an infrastructure BSS network or by the network peer for an independent BSS network (ad hoc network), the information returned should not be trusted. The <b>ulIeOffset</b> and <b>ulIeSize</b>  members in the <a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a> structure should be used to determine the maximum size of the information element data blob in the <b>WLAN_BSS_ENTRY</b> structure, not the data in the information element data blob. 




## -see-also




<a href="https://msdn.microsoft.com/82883cea-515b-426d-9961-c144ce99b3db">WLAN_AVAILABLE_NETWORK</a>



<a href="https://msdn.microsoft.com/0ac508b2-9117-423d-89d3-982f070c70e2">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a>



<a href="https://msdn.microsoft.com/27353a1b-2a3c-4c3b-b512-917d010ee8dd">WlanGetAvailableNetworkList</a>



<a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a>
 

 

