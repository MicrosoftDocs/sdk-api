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

# _DDGETSURFACESTATEOUT structure


## -description


The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff550673">DD_DXAPI_GET_SURFACE_STATE</a> operations. A return code of DD_OK indicates success.


### -field dwStateCaps

Contains the DirectDrawSurface's capabilities of the device. One or more of the following:

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
The device is capable of performing bob mode.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
The device is capable of performing weave mode.

</td>
</tr>
</table>
 


### -field dwStateStatus

Contains the status of the selected DirectDrawSurface. One or more of the following:

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
Bob mode is being used on this surface.

</td>
</tr>
<tr>
<td>
DDSTATE_EXPLICITLY_SET

</td>
<td>
This state is due to a previous <a href="https://msdn.microsoft.com/library/windows/hardware/ff551504">DD_DXAPI_SET_SURFACE_STATE</a> call.

</td>
</tr>
<tr>
<td>
DDSTATE_SKIPEVENFIELDS

</td>
<td>
Stop bob or weave mode and skip every other field instead.

</td>
</tr>
<tr>
<td>
DDSTATE_SOFTWARE_AUTOFLIP

</td>
<td>
Software (as opposed to hardware) autoflipping is being used.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
Weave mode is being used on this surface.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550673">DD_DXAPI_GET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

