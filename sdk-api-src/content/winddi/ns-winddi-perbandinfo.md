---
UID: NS:winddi._PERBANDINFO
title: PERBANDINFO (winddi.h)
description: The PERBANDINFO structure is used as input to a printer graphics DLL's DrvQueryPerBandInfo function.
helpviewer_keywords: ["*PPERBANDINFO","PERBANDINFO","PERBANDINFO structure [Display Devices]","PPERBANDINFO","PPERBANDINFO structure pointer [Display Devices]","display.perbandinfo","grstrcts_130088d9-975d-4b22-be85-90e129c64455.xml","winddi/PERBANDINFO","winddi/PPERBANDINFO"]
old-location: display\perbandinfo.htm
tech.root: display
ms.assetid: ec02542f-68d1-4d05-a4d1-e475725997ad
ms.date: 12/05/2018
ms.keywords: '*PPERBANDINFO, PERBANDINFO, PERBANDINFO structure [Display Devices], PPERBANDINFO, PPERBANDINFO structure pointer [Display Devices], display.perbandinfo, grstrcts_130088d9-975d-4b22-be85-90e129c64455.xml, winddi/PERBANDINFO, winddi/PPERBANDINFO'
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
req.typenames: PERBANDINFO, *PPERBANDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERBANDINFO
 - winddi/_PERBANDINFO
 - PPERBANDINFO
 - winddi/PPERBANDINFO
 - PERBANDINFO
 - winddi/PERBANDINFO
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
 - PERBANDINFO
---

# PERBANDINFO structure


## -description

The PERBANDINFO structure is used as input to a printer graphics DLL's <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryperbandinfo">DrvQueryPerBandInfo</a> function.

## -struct-fields

### -field bRepeatThisBand

If <b>TRUE</b>, GDI redraws the previous band. If <b>FALSE</b>, GDI draws the next band.

### -field szlBand

Specifies a SIZEL structure that contains the width and height, in pixels, of the rectangle in which GDI can draw the band. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -field ulHorzRes

Specifies the horizontal resolution GDI should use when scaling the band.

### -field ulVertRes

Specifies the vertical resolution GDI should use when scaling the band.

## -remarks

If the result of <b>ulHorzRes</b> divided by <b>ulVertRes</b> is smaller than the result obtained by dividing the same members of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure, the band is rendered smaller by the graphics engine. If the values are the same, no scaling is done. The resultant scale factor obtained from this structure cannot be larger than the one stored in GDIINFO.

When the band is scaled, the graphics engine anchors the smaller band to the upper-left corner of the original band.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryperbandinfo">DrvQueryPerBandInfo</a>



<a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>