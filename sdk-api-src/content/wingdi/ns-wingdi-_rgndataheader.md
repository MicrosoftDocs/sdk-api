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

# _RGNDATAHEADER structure


## -description



The <b>RGNDATAHEADER</b> structure describes the data returned by the <a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a> function.




## -struct-fields




### -field dwSize

The size, in bytes, of the header.


### -field iType

The type of region. This value must be RDH_RECTANGLES.


### -field nCount

The number of rectangles that make up the region.


### -field nRgnSize

The size of the <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> buffer required to receive the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures that make up the region. If the size is not known, this member can be zero.


### -field rcBound

A bounding rectangle for the region in logical units.


## -see-also




<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>



<a href="https://msdn.microsoft.com/e66d46fd-af6f-43ce-a9f7-21389d14cb89">Region Structures</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

