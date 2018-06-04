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

# _RUN structure


## -description


The RUN structure is used to describe a linear set of pixels that is not clipped by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539416">CLIPLINE</a> structure.


## -struct-fields




### -field iStart

Specifies the starting point for a field of pixels to be drawn. The first pixel of the unclipped line is pixel 0.


### -field iStop

Specifies the stopping point for a field of pixels to be drawn.


## -remarks



If the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> is complex, a single line segment can be broken into many RUNs. The same segment is returned as many times as necessary to list all of its RUNs.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>
 

 

