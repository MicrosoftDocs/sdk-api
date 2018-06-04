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

# _AM_INTF_SEARCH_FLAGS enumeration


## -description



Specifies the types of object to search, when attempting to find an interface on the filter graph.




## -enum-fields




### -field AM_INTF_SEARCH_INPUT_PIN

Search input pins.


### -field AM_INTF_SEARCH_OUTPUT_PIN

Search output pins.


### -field AM_INTF_SEARCH_FILTER

Search filters.


## -remarks



If no flags are set (the default case), it is equivalent to the bitwise <b>OR</b> of all the flags. All filters and pins are searched.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23106ef0-e5ce-47a6-97b0-518bb78ec67c">IAMGraphStreams::FindUpstreamInterface</a>
 

 

