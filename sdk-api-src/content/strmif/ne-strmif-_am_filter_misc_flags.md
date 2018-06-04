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

# _AM_FILTER_MISC_FLAGS enumeration


## -description



The <b>_AM_FILTER_MISC_FLAGS</b> enumeration contains flags that indicate whether a filter is a source filter or a renderer filter.




## -enum-fields




### -field AM_FILTER_MISC_FLAGS_IS_RENDERER

The filter is a renderer and sends an <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> event at the end of the stream.


### -field AM_FILTER_MISC_FLAGS_IS_SOURCE

The filter is a source filter.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/03728d28-a3e5-4ac5-b637-1daa173e5e88">IAMFilterMiscFlags::GetMiscFlags</a>
 

 

