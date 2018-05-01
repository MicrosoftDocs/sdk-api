---
UID: NS:wlanapi._WLAN_INTERFACE_INFO_LIST
title: "_WLAN_INTERFACE_INFO_LIST"
author: windows-driver-content
description: Array of NIC interface information.
old-location: nwifi\wlan_interface_info_list.htm
old-project: NativeWiFi
ms.assetid: c57f4658-9f1e-4b05-a298-38a064121bb3
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PWLAN_INTERFACE_INFO_LIST, PWLAN_INTERFACE_INFO_LIST, PWLAN_INTERFACE_INFO_LIST structure pointer [NativeWIFI], WLAN_INTERFACE_INFO_LIST, WLAN_INTERFACE_INFO_LIST structure [NativeWIFI], _WLAN_INTERFACE_INFO_LIST, nwifi.wlan_interface_info_list, wlanapi/PWLAN_INTERFACE_INFO_LIST, wlanapi/WLAN_INTERFACE_INFO_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WLAN_INTERFACE_INFO_LIST, *PWLAN_INTERFACE_INFO_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_INTERFACE_INFO_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_INTERFACE_INFO_LIST structure


## -description


The <b>WLAN_INTERFACE_INFO_LIST</b> structure contains an array of NIC interface information.


## -struct-fields




### -field dwNumberOfItems

Contains the number of items in the <b>InterfaceInfo</b> member.


### -field dwIndex

The index of the current item.  The index of the first item is 0. <b>dwIndex</b> must be less than <b>dwNumberOfItems</b>.

This member is not used by the wireless service. Applications can use this member when processing individual interfaces in the  <b>WLAN_INTERFACE_INFO_LIST</b> structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.


### -field InterfaceInfo

An array of <a href="https://msdn.microsoft.com/906e7d59-ebd0-47e7-985e-f5d313f19ecb">WLAN_INTERFACE_INFO</a> structures containing interface information.


## -see-also




<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>
 

 

