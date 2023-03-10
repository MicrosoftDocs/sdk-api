---
UID: NS:dxmini._DDFLIPVIDEOPORTINFO
title: DDFLIPVIDEOPORTINFO (dxmini.h)
description: The DDFLIPVIDEOPORTINFO structure contains the video port extensions (VPE) object and surface information.
helpviewer_keywords: ["*PDDFLIPVIDEOPORTINFO","DDFLIPVIDEOPORTINFO","DDFLIPVIDEOPORTINFO structure [Display Devices]","PDDFLIPVIDEOPORTINFO","PDDFLIPVIDEOPORTINFO structure pointer [Display Devices]","Video_Structs_e5e5e93f-25a2-47a6-a99c-6ac8ca43f069.xml","display.ddflipvideoportinfo","dxmini/DDFLIPVIDEOPORTINFO","dxmini/PDDFLIPVIDEOPORTINFO"]
old-location: display\ddflipvideoportinfo.htm
tech.root: display
ms.assetid: 9cf87d19-2db6-48f8-96a6-2b6ac969c774
ms.date: 12/05/2018
ms.keywords: '*PDDFLIPVIDEOPORTINFO, DDFLIPVIDEOPORTINFO, DDFLIPVIDEOPORTINFO structure [Display Devices], PDDFLIPVIDEOPORTINFO, PDDFLIPVIDEOPORTINFO structure pointer [Display Devices], Video_Structs_e5e5e93f-25a2-47a6-a99c-6ac8ca43f069.xml, display.ddflipvideoportinfo, dxmini/DDFLIPVIDEOPORTINFO, dxmini/PDDFLIPVIDEOPORTINFO'
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
req.typenames: DDFLIPVIDEOPORTINFO, *PDDFLIPVIDEOPORTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDFLIPVIDEOPORTINFO
 - dxmini/_DDFLIPVIDEOPORTINFO
 - PDDFLIPVIDEOPORTINFO
 - dxmini/PDDFLIPVIDEOPORTINFO
 - DDFLIPVIDEOPORTINFO
 - dxmini/DDFLIPVIDEOPORTINFO
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
 - DDFLIPVIDEOPORTINFO
---

# DDFLIPVIDEOPORTINFO structure


## -description

The DDFLIPVIDEOPORTINFO structure contains the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object and surface information.

## -struct-fields

### -field lpVideoPortData

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a> structure that contains the VPE object information.

### -field lpCurrentSurface

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a> structure that contains information about the current surface.

### -field lpTargetSurface

Points to a DDSURFACEDATA structure that contains information about the target surface.

### -field dwFlipVPFlags

Indicates whether the surfaces represent <a href="/windows-hardware/drivers/">vertical blanking interval (VBI)</a> surfaces or regular surfaces. One of the following: 

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
Flip the VBI surface.

</td>
</tr>
<tr>
<td>
DDVPFLIP_VIDEO

</td>
<td>
Flip the normal video surface.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a>



<a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipvideoport">DxFlipVideoPort</a>