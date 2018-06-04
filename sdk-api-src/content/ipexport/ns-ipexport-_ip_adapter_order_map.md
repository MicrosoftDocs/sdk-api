---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _IP_ADAPTER_ORDER_MAP structure


## -description


The <b>IP_ADAPTER_ORDER_MAP</b> structure stores an array of information about adapters and their relative priority on the local computer.


## -struct-fields




### -field NumAdapters

The number of network adapters in the <b>AdapterOrder</b> member.


### -field AdapterOrder

An array of adapter indexes  on the local computer, provided in the order specified in the <b>Adapters and Bindings</b> dialog box for <b>Network Connections</b>. 


## -remarks



This structure is returned by the GetAdapterOrderMap function, and is used as a tie breaker for otherwise equal interfaces during network operations. The GetAdapterOrderMap function should not be called directly; use the GetAdaptersInfo function instead.

The <b>IP_ADAPTER_ORDER_MAP</b> structure contains at least one <b>AdapterOrder</b> member even if the <b>NumAdapters</b> member of the <b>IP_ADAPTER_ORDER_MAP</b> structure indicates no network adapters. When the <b>NumAdapters</b> member of the <b>IP_ADAPTER_ORDER_MAP</b> structure is zero, the value of the single  <b>AdapterOrder</b> member is undefined. 

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.




## -see-also




GetAdapterOrderMap



GetAdaptersInfo
 

 

