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

# _DHCP_FILTER_ADD_INFOV4 structure


## -description


The <b>DHCP_FILTER_ADD_INFO</b> structure contains information regarding the link-layer filter to be added to the allow and deny filter list.


## -struct-fields




### -field AddrPatt


<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a> structure that contains the address/pattern-related information of the link-layer filter.


### -field Comment

Pointer to a Unicode string that contains a text comment for the filter.


### -field ListType


<a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a> enumeration value that specifies the list type to which the filter is to be added.


## -see-also




<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a>



<a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a>
 

 

