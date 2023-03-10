---
UID: NS:winddi._CLIPLINE
title: CLIPLINE (winddi.h)
description: The CLIPLINE structure gives the driver access to a portion of a line between two clip regions used for drawing.
helpviewer_keywords: ["*PCLIPLINE","CLIPLINE","CLIPLINE structure [Display Devices]","PCLIPLINE","PCLIPLINE structure pointer [Display Devices]","display.clipline","grstrcts_01e6e35a-79ca-4dba-866e-24306b83cb51.xml","winddi/CLIPLINE","winddi/PCLIPLINE"]
old-location: display\clipline.htm
tech.root: display
ms.assetid: ec938519-3c0c-4664-9e9a-b7fb338920f5
ms.date: 12/05/2018
ms.keywords: '*PCLIPLINE, CLIPLINE, CLIPLINE structure [Display Devices], PCLIPLINE, PCLIPLINE structure pointer [Display Devices], display.clipline, grstrcts_01e6e35a-79ca-4dba-866e-24306b83cb51.xml, winddi/CLIPLINE, winddi/PCLIPLINE'
req.header: winddi.h
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
req.typenames: CLIPLINE, *PCLIPLINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLIPLINE
 - winddi/_CLIPLINE
 - PCLIPLINE
 - winddi/PCLIPLINE
 - CLIPLINE
 - winddi/CLIPLINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - CLIPLINE
---

# CLIPLINE structure


## -description

The CLIPLINE structure gives the driver access to a portion of a line between two <a href="/windows-hardware/drivers/">clip regions</a> used for drawing.

## -struct-fields

### -field ptfxA

Specifies a POINTFIX structure that contains the starting point of the line.

### -field ptfxB

Specifies a POINTFIX structure that contains the end point of the line.

### -field lStyleState

Is a pair of 16-bit values supplied by GDI whenever the driver calls <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>. These two values are packed into a LONG and specify the style offset back to the first pixel of the line segment. This is the first pixel that would be rendered if the line were not clipped. This value allows the styling for the remainder of the line to be computed. Refer to <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a> for additional information.

### -field c

Specifies the number of RUN structures in the <b>arun</b> array.

### -field arun

Is an array of <a href="/windows/desktop/api/winddi/ns-winddi-run">RUN</a> structures. The RUN structures describe the start and stop portions of the clip line.

## -remarks

The CLIPLINE structure is used by <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>. The CLIPLINE structure contains the original, unclipped control points of the line segment.

See <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a> for a description of the POINTFIX structure.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>



<a href="/windows/desktop/api/winddi/ns-winddi-run">RUN</a>