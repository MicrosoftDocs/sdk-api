---
UID: NS:ddrawint._DD_SURFACE_LOCAL
title: DD_SURFACE_LOCAL (ddrawint.h)
description: The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object.
helpviewer_keywords: ["*PDD_SURFACE_LOCAL","DD_SURFACE_LOCAL","DD_SURFACE_LOCAL structure [Display Devices]","ddrawint/DD_SURFACE_LOCAL","ddstrcts_07a504fc-c8bb-4b48-b825-4da3012e4f95.xml","display.dd_surface_local"]
old-location: display\dd_surface_local.htm
tech.root: display
ms.assetid: 45a41cec-0257-4e26-809d-c2fc4c247328
ms.date: 12/05/2018
ms.keywords: '*PDD_SURFACE_LOCAL, DD_SURFACE_LOCAL, DD_SURFACE_LOCAL structure [Display Devices], ddrawint/DD_SURFACE_LOCAL, ddstrcts_07a504fc-c8bb-4b48-b825-4da3012e4f95.xml, display.dd_surface_local'
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
targetos: Windows
req.typenames: '*PDD_SURFACE_LOCAL, DD_SURFACE_LOCAL'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SURFACE_LOCAL
 - ddrawint/_DD_SURFACE_LOCAL
 - PDD_SURFACE_LOCAL
 - ddrawint/PDD_SURFACE_LOCAL
 - DD_SURFACE_LOCAL
 - ddrawint/DD_SURFACE_LOCAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SURFACE_LOCAL
---

# DD_SURFACE_LOCAL structure


## -description

The DD_SURFACE_LOCAL structure contains surface-related data that is unique to an individual surface object.

## -struct-fields

### -field lpGbl

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_global">DD_SURFACE_GLOBAL</a> structure containing surface data that is shared globally with multiple surfaces.

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

Specifies a <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure that describes the capabilities of the surface.

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

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_more">DD_SURFACE_MORE</a> structure that contains additional local surface data.

### -field lpAttachList

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_attachlist">DD_ATTACHLIST</a> structure that contains the list of surfaces to which this surface attached.

### -field lpAttachListFrom

Points to a DD_ATTACHLIST structure that contains the list of surfaces attached to this surface.

### -field rcOverlaySrc

Reserved for system use and should be ignored by the driver.