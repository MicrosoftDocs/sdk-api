---
UID: NS:wlanapi._DOT11_NETWORK_LIST
title: DOT11_NETWORK_LIST (wlanapi.h)
author: windows-sdk-content
description: Contains a list of 802.11 wireless networks.
old-location: nwifi\dot11_network_list.htm
tech.root: NativeWiFi
ms.assetid: 607c5795-8168-4c6b-a2f3-65f31aea5cf5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDOT11_NETWORK_LIST, DOT11_NETWORK_LIST, DOT11_NETWORK_LIST structure [NativeWIFI], PDOT11_NETWORK_LIST, PDOT11_NETWORK_LIST structure pointer [NativeWIFI], nwifi.dot11_network_list, wlanapi/DOT11_NETWORK_LIST, wlanapi/PDOT11_NETWORK_LIST"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - DOT11_NETWORK_LIST
product: Windows
targetos: Windows
req.typenames: DOT11_NETWORK_LIST, *PDOT11_NETWORK_LIST
req.redist: 
ms.custom: 19H1
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

An array of <a href="https://msdn.microsoft.com/95f58433-deef-4c47-8f6c-a9e7b0d52dad">DOT11_NETWORK</a> structures that contain 802.11 wireless network information.


## -see-also




<a href="https://msdn.microsoft.com/95f58433-deef-4c47-8f6c-a9e7b0d52dad">DOT11_NETWORK</a>



<a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a>



<a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a>
 

 

