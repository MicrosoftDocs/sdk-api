---
UID: NS:ddkmapi._DDFLIPVIDEOPORT
title: DDFLIPVIDEOPORT (ddkmapi.h)
description: The DDFLIPVIDEOPORT structure contains the information required to flip the hardware video port.
helpviewer_keywords: ["*LPDDFLIPVIDEOPORT","DDFLIPVIDEOPORT","DDFLIPVIDEOPORT structure [Display Devices]","LPDDFLIPVIDEOPORT","LPDDFLIPVIDEOPORT structure pointer [Display Devices]","ddkmapi/DDFLIPVIDEOPORT","ddkmapi/LPDDFLIPVIDEOPORT","ddstrcts_b6a3e4ea-217b-40d5-a829-c9ca62632a3e.xml","display.ddflipvideoport"]
old-location: display\ddflipvideoport.htm
tech.root: display
ms.assetid: c30c100c-8c91-44e2-b75b-92ce73d44047
ms.date: 12/05/2018
ms.keywords: '*LPDDFLIPVIDEOPORT, DDFLIPVIDEOPORT, DDFLIPVIDEOPORT structure [Display Devices], LPDDFLIPVIDEOPORT, LPDDFLIPVIDEOPORT structure pointer [Display Devices], ddkmapi/DDFLIPVIDEOPORT, ddkmapi/LPDDFLIPVIDEOPORT, ddstrcts_b6a3e4ea-217b-40d5-a829-c9ca62632a3e.xml, display.ddflipvideoport'
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
req.typenames: DDFLIPVIDEOPORT, *LPDDFLIPVIDEOPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDFLIPVIDEOPORT
 - ddkmapi/_DDFLIPVIDEOPORT
 - LPDDFLIPVIDEOPORT
 - ddkmapi/LPDDFLIPVIDEOPORT
 - DDFLIPVIDEOPORT
 - ddkmapi/DDFLIPVIDEOPORT
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
 - DDFLIPVIDEOPORT
---

# DDFLIPVIDEOPORT structure


## -description

The DDFLIPVIDEOPORT structure contains the information required to flip the hardware video port.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.

### -field hVideoPort

Specifies the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object handle.

### -field hCurrentSurface

Specifies the current DirectDrawSurface handle.

### -field hTargetSurface

Specifies the handle of the DirectDrawSurface to which the flip occurs.

### -field dwFlags

Indicates whether the surfaces represent <a href="/windows-hardware/drivers/">VBI</a> surfaces or regular surfaces. One of the following: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPFLIP_VBI

</td>
<td>
Flips the VBI surface.

</td>
</tr>
<tr>
<td>
DDVPFLIP_VIDEO

</td>
<td>
Flips the normal video surface.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550618(v=vs.85)">DD_DXAPI_FLIP_VP</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>