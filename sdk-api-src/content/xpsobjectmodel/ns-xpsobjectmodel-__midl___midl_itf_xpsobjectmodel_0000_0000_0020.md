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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020 structure


## -description


This structure describes a dash element of a path.


## -struct-fields




### -field length

Length of the visible segment of the dash element.


### -field gap

Length of the space between the visible segments of the dash sequence.


## -remarks



The length must be non-negative and is measured in multiples of the path's stroke thickness.

 Values of <b>length</b> do not include the end caps of the visible segments.

The shape of the end caps of the visible segments is determined by the <a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a> value.




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a>
 

 

