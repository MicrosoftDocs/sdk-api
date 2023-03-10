---
UID: NS:wlanapi._WLAN_INTERFACE_INFO_LIST
title: WLAN_INTERFACE_INFO_LIST (wlanapi.h)
description: Array of NIC interface information.
helpviewer_keywords: ["*PWLAN_INTERFACE_INFO_LIST","PWLAN_INTERFACE_INFO_LIST","PWLAN_INTERFACE_INFO_LIST structure pointer [NativeWIFI]","WLAN_INTERFACE_INFO_LIST","WLAN_INTERFACE_INFO_LIST structure [NativeWIFI]","nwifi.wlan_interface_info_list","wlanapi/PWLAN_INTERFACE_INFO_LIST","wlanapi/WLAN_INTERFACE_INFO_LIST"]
old-location: nwifi\wlan_interface_info_list.htm
tech.root: nwifi
ms.assetid: c57f4658-9f1e-4b05-a298-38a064121bb3
ms.date: 12/05/2018
ms.keywords: '*PWLAN_INTERFACE_INFO_LIST, PWLAN_INTERFACE_INFO_LIST, PWLAN_INTERFACE_INFO_LIST structure pointer [NativeWIFI], WLAN_INTERFACE_INFO_LIST, WLAN_INTERFACE_INFO_LIST structure [NativeWIFI], nwifi.wlan_interface_info_list, wlanapi/PWLAN_INTERFACE_INFO_LIST, wlanapi/WLAN_INTERFACE_INFO_LIST'
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
req.typenames: WLAN_INTERFACE_INFO_LIST, *PWLAN_INTERFACE_INFO_LIST
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_INTERFACE_INFO_LIST
 - wlanapi/_WLAN_INTERFACE_INFO_LIST
 - PWLAN_INTERFACE_INFO_LIST
 - wlanapi/PWLAN_INTERFACE_INFO_LIST
 - WLAN_INTERFACE_INFO_LIST
 - wlanapi/WLAN_INTERFACE_INFO_LIST
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
 - WLAN_INTERFACE_INFO_LIST
---

# WLAN_INTERFACE_INFO_LIST structure


## -description

The <b>WLAN_INTERFACE_INFO_LIST</b> structure contains an array of NIC interface information.

## -struct-fields

### -field dwNumberOfItems

Contains the number of items in the <b>InterfaceInfo</b> member.

### -field dwIndex

The index of the current item.  The index of the first item is 0. <b>dwIndex</b> must be less than <b>dwNumberOfItems</b>.

This member is not used by the wireless service. Applications can use this member when processing individual interfaces in the  <b>WLAN_INTERFACE_INFO_LIST</b> structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.

### -field InterfaceInfo.unique

### -field InterfaceInfo.size_is

### -field InterfaceInfo.size_is.dwNumberOfItems

### -field InterfaceInfo

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_info">WLAN_INTERFACE_INFO</a> structures containing interface information.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>