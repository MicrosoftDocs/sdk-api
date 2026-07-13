---
UID: NS:ddkmapi._DDSETSURFACETATE
title: DDSETSURFACESTATE (ddkmapi.h)
description: The DDSETSURFACESTATE structure contains the surface state information.
helpviewer_keywords: ["*LPDDSETSURFACESTATE","DDSETSURFACESTATE","DDSETSURFACESTATE structure [Display Devices]","LPDDSETSURFACESTATE","LPDDSETSURFACESTATE structure pointer [Display Devices]","ddkmapi/DDSETSURFACESTATE","ddkmapi/LPDDSETSURFACESTATE","ddstrcts_ddf8814f-d375-4b3c-93dc-0a77d12f3aab.xml","display.ddsetsurfacestate"]
old-location: display\ddsetsurfacestate.htm
tech.root: display
ms.assetid: a54b1496-1f7e-4ba9-acb3-2debbe7e980d
ms.date: 12/05/2018
ms.keywords: '*LPDDSETSURFACESTATE, DDSETSURFACESTATE, DDSETSURFACESTATE structure [Display Devices], LPDDSETSURFACESTATE, LPDDSETSURFACESTATE structure pointer [Display Devices], ddkmapi/DDSETSURFACESTATE, ddkmapi/LPDDSETSURFACESTATE, ddstrcts_ddf8814f-d375-4b3c-93dc-0a77d12f3aab.xml, display.ddsetsurfacestate'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDSETSURFACESTATE, *LPDDSETSURFACESTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSETSURFACETATE
 - ddkmapi/_DDSETSURFACETATE
 - LPDDSETSURFACESTATE
 - ddkmapi/LPDDSETSURFACESTATE
 - DDSETSURFACESTATE
 - ddkmapi/DDSETSURFACESTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDSETSURFACESTATE
---

# DDSETSURFACESTATE structure


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

<a href="/previous-versions/windows/hardware/drivers/ff551504(v=vs.85)">DD_DXAPI_SET_SURFACE_STATE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>