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

# _EVENT_MAP_ENTRY structure


## -description



		Defines a single value map entry. 


## -struct-fields




### -field OutputOffset

Offset from the beginning of the <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a> structure to a null-terminated Unicode string that contains the string associated with the map value in <b>Value</b> or <b>InputOffset</b>.


### -field Value

If the <b>MapEntryValueType</b> member of <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>  is EVENTMAP_ENTRY_VALUETYPE_ULONG, use this member to access the map value.


### -field InputOffset

Offset from the beginning of the <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a> structure to the null-terminated Unicode string that contains the map value.

The offset is used for pattern maps and WMI value maps that map strings to strings. 


## -remarks



For maps defined in a manifest, the string will contain a space at the end of the string. For example, if the value is mapped to "Monday" in the manifest, the string is returned as "Monday ".




## -see-also




<a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>
 

 

