---
UID: NS:ddkmapi._DDFLIPOVERLAY
title: DDFLIPOVERLAY (ddkmapi.h)
description: The DDFLIPOVERLAY structure contains the surface information required for the flip.
helpviewer_keywords: ["*LPDDFLIPOVERLAY","DDFLIPOVERLAY","DDFLIPOVERLAY structure [Display Devices]","LPDDFLIPOVERLAY","LPDDFLIPOVERLAY structure pointer [Display Devices]","ddkmapi/DDFLIPOVERLAY","ddkmapi/LPDDFLIPOVERLAY","ddstrcts_a29d7c69-b024-435d-8853-54477c17e960.xml","display.ddflipoverlay"]
old-location: display\ddflipoverlay.htm
tech.root: display
ms.assetid: 455005d8-5713-4188-9bcb-333c7c4f849d
ms.date: 12/05/2018
ms.keywords: '*LPDDFLIPOVERLAY, DDFLIPOVERLAY, DDFLIPOVERLAY structure [Display Devices], LPDDFLIPOVERLAY, LPDDFLIPOVERLAY structure pointer [Display Devices], ddkmapi/DDFLIPOVERLAY, ddkmapi/LPDDFLIPOVERLAY, ddstrcts_a29d7c69-b024-435d-8853-54477c17e960.xml, display.ddflipoverlay'
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
req.typenames: DDFLIPOVERLAY, *LPDDFLIPOVERLAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDFLIPOVERLAY
 - ddkmapi/_DDFLIPOVERLAY
 - LPDDFLIPOVERLAY
 - ddkmapi/LPDDFLIPOVERLAY
 - DDFLIPOVERLAY
 - ddkmapi/DDFLIPOVERLAY
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
 - DDFLIPOVERLAY
---

# DDFLIPOVERLAY structure


## -description

The DDFLIPOVERLAY structure contains the surface information required for the flip.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.

### -field hCurrentSurface

Specifies the current DirectDrawSurface handle.

### -field hTargetSurface

Handle of the DirectDrawSurface to which the flip occurs.

### -field dwFlags

Flags specifying flip options. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDFLIP_EVEN

</td>
<td>
For use only when displaying video in an overlay surface. The new surface contains data from the even field of a video signal. This flag cannot be used with the DDFLIP_ODD flag.

</td>
</tr>
<tr>
<td>
DDFLIP_ODD

</td>
<td>
For use only when displaying video in an overlay surface. The new surface contains data from the odd field of a video signal. This flag cannot be used with the DDFLIP_EVEN flag.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550612(v=vs.85)">DD_DXAPI_FLIP_OVERLAY</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>