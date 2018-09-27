---
UID: NS:ddrawint._DD_SURFACE_LOCAL
title: "_DD_SURFACE_LOCAL"
author: windows-sdk-content
description: The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object.
old-location: display\dd_surface_local.htm
tech.root: display
ms.assetid: 45a41cec-0257-4e26-809d-c2fc4c247328
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PDD_SURFACE_LOCAL, DD_SURFACE_LOCAL, DD_SURFACE_LOCAL structure [Display Devices], _DD_SURFACE_LOCAL, ddrawint/DD_SURFACE_LOCAL, ddstrcts_07a504fc-c8bb-4b48-b825-4da3012e4f95.xml, display.dd_surface_local"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SURFACE_LOCAL
product: Windows
targetos: Windows
req.typenames: "*PDD_SURFACE_LOCAL, DD_SURFACE_LOCAL"
req.redist: 
---

# _DD_SURFACE_LOCAL structure


## -description


The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object.


## -struct-fields




### -field lpGbl

Points to the <a href="https://msdn.microsoft.com/11e0a6b9-16b9-4fc3-8e17-776f56c12196">DD_SURFACE_GLOBAL</a> structure containing surface data that is shared globally with multiple surfaces.


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

Specifies a <a href="https://msdn.microsoft.com/e1ed1fa2-2f3c-4d04-a601-c11fb77eb5cc">DDSCAPS</a> structure that describes the capabilities of the surface.


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

Points to a <a href="https://msdn.microsoft.com/4b000d0f-4ff1-4155-92be-b56793978b1f">DD_SURFACE_MORE</a> structure that contains additional local surface data.


### -field lpAttachList

Points to a <a href="https://msdn.microsoft.com/d79b9277-ef71-4ef8-804c-d5bc8f772d0f">DD_ATTACHLIST</a> structure that contains the list of surfaces to which this surface attached. 


### -field lpAttachListFrom

Points to a DD_ATTACHLIST structure that contains the list of surfaces attached to this surface. 


### -field rcOverlaySrc

Reserved for system use and should be ignored by the driver. 

