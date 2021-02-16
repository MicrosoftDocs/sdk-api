---
UID: NS:dxmini._DDFLIPOVERLAYINFO
title: DDFLIPOVERLAYINFO (dxmini.h)
description: The DDFLIPOVERLAYINFO structure contains the flip information for the surface.
helpviewer_keywords: ["*PDDFLIPOVERLAYINFO","DDFLIPOVERLAYINFO","DDFLIPOVERLAYINFO structure [Display Devices]","PDDFLIPOVERLAYINFO","PDDFLIPOVERLAYINFO structure pointer [Display Devices]","Video_Structs_c9d5aaff-82e8-482e-b774-6c14f0fa8610.xml","display.ddflipoverlayinfo","dxmini/DDFLIPOVERLAYINFO","dxmini/PDDFLIPOVERLAYINFO"]
old-location: display\ddflipoverlayinfo.htm
tech.root: display
ms.assetid: 04e4baba-4b6c-4f0a-8197-1fb2d83f53d6
ms.date: 12/05/2018
ms.keywords: '*PDDFLIPOVERLAYINFO, DDFLIPOVERLAYINFO, DDFLIPOVERLAYINFO structure [Display Devices], PDDFLIPOVERLAYINFO, PDDFLIPOVERLAYINFO structure pointer [Display Devices], Video_Structs_c9d5aaff-82e8-482e-b774-6c14f0fa8610.xml, display.ddflipoverlayinfo, dxmini/DDFLIPOVERLAYINFO, dxmini/PDDFLIPOVERLAYINFO'
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DDFLIPOVERLAYINFO, *PDDFLIPOVERLAYINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDFLIPOVERLAYINFO
 - dxmini/_DDFLIPOVERLAYINFO
 - PDDFLIPOVERLAYINFO
 - dxmini/PDDFLIPOVERLAYINFO
 - DDFLIPOVERLAYINFO
 - dxmini/DDFLIPOVERLAYINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDFLIPOVERLAYINFO
---

# DDFLIPOVERLAYINFO structure


## -description

The DDFLIPOVERLAYINFO structure contains the flip information for the surface.

## -struct-fields

### -field lpCurrentSurface

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a> structure that contains information about the current surface.

### -field lpTargetSurface

Points to a DDSURFACEDATA structure that contains information about the target surface.

### -field dwFlags

Specifies the polarity of the data in the field being flipped. One of the following flags is returned: 

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
The target surface contains the even field of video data.

</td>
</tr>
<tr>
<td>
DDFLIP_ODD

</td>
<td>
The target surface contains the odd field of video data.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipoverlay">DxFlipOverlay</a>