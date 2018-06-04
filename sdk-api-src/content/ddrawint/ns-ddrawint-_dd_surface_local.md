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

# _DD_SURFACE_LOCAL structure


## -description


The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object.


## -struct-fields




### -field lpGbl

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551726">DD_SURFACE_GLOBAL</a> structure containing surface data that is shared globally with multiple surfaces.


### -field dwFlags

Specifies a set of surface flags. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDRAWISURF_BACKBUFFER

</td>
<td>
The surface was originally a back buffer.

</td>
</tr>
<tr>
<td>
DDRAWISURF_DRIVERMANAGED

</td>
<td>
The surface is a driver managed texture used with Microsoft Direct3D.

</td>
</tr>
<tr>
<td>
DDRAWISURF_FRONTBUFFER

</td>
<td>
The surface was originally a front buffer.

</td>
</tr>
<tr>
<td>
DDRAWISURF_HASCKEYSRCBLT

</td>
<td>
The surface has source color key overlay data in the <b>ddckCKSrcBlt</b> member.

</td>
</tr>
<tr>
<td>
DDRAWISURF_HASOVERLAYDATA

</td>
<td>
The surface has overlay data.

</td>
</tr>
<tr>
<td>
DDRAWISURF_HASPIXELFORMAT

</td>
<td>
The surface has pixel format data.

</td>
</tr>
<tr>
<td>
DDRAWISURF_INVALID

</td>
<td>
The surface has been invalidated by a mode setting operation.

</td>
</tr>
</table>
 


### -field ddsCaps

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure that describes the capabilities of the surface.


### -field dwReserved1

Reserved for use by the display driver.


### -field ddckCKSrcOverlay

Specifies a DDCOLORKEY structure (defined in the Microsoft DirectDraw SDK documentation) that contains the color key information for source overlay use.


### -field ddckCKSrcBlt

Specifies a DDCOLORKEY structure that describes the color key for source color key overlays. 


### -field ddckCKDestOverlay

Specifies a DDCOLORKEY structure that contains the color key information for destination overlay use.


### -field ddckCKDestBlt

Specifies a DDCOLORKEY structure that describes the color key for destination color key overlays.


### -field lpSurfMore

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551737">DD_SURFACE_MORE</a> structure that contains additional local surface data.


### -field lpAttachList

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550466">DD_ATTACHLIST</a> structure that contains the list of surfaces to which this surface attached. 


### -field lpAttachListFrom

Points to a DD_ATTACHLIST structure that contains the list of surfaces attached to this surface. 


### -field rcOverlaySrc

Reserved for system use and should be ignored by the driver. 

