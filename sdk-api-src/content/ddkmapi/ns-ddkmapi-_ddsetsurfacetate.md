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

# _DDSETSURFACETATE structure


## -description


The DDSETSURFACESTATE structure contains the surface state information. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.


### -field hSurface

Specifies the DirectDrawSurface handle.


### -field dwState

Indicates the surface state. One of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSTATE_BOB

</td>
<td>
Bob mode is to be used on this surface.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
Weave mode is to be used on this surface.

</td>
</tr>
</table>
 


### -field dwStartField

Indicates the field on which the state change should occur. A value of 0 indicates it should occur at the start of the next field, a value of 1 indicates the start of the following field, and so on.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551504">DD_DXAPI_SET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

