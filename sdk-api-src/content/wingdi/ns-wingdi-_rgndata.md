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

# _RGNDATA structure


## -description



The <b>RGNDATA</b> structure contains a header and an array of rectangles that compose a region. The rectangles are sorted top to bottom, left to right. They do not overlap.




## -struct-fields




### -field rdh

A <a href="https://msdn.microsoft.com/15990903-8a48-4c47-b527-269d775255a5">RGNDATAHEADER</a> structure. The members of this structure specify the type of region (whether it is rectangular or trapezoidal), the number of rectangles that make up the region, the size of the buffer that contains the rectangle structures, and so on.


### -field Buffer

Specifies an arbitrary-size buffer that contains the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures that make up the region.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/15990903-8a48-4c47-b527-269d775255a5">RGNDATAHEADER</a>



<a href="https://msdn.microsoft.com/e66d46fd-af6f-43ce-a9f7-21389d14cb89">Region Structures</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

