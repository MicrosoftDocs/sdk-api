---
UID: NS:wingdi.tagEMRSTRETCHBLT
title: EMRSTRETCHBLT (wingdi.h)
description: The EMRSTRETCHBLT structure contains members for the StretchBlt enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.
helpviewer_keywords: ["*PEMRSTRETCHBLT","EMRSTRETCHBLT","EMRSTRETCHBLT structure [Windows GDI]","PEMRSTRETCHBLT","PEMRSTRETCHBLT structure pointer [Windows GDI]","_win32_EMRSTRETCHBLT_str","gdi.emrstretchblt","wingdi/EMRSTRETCHBLT","wingdi/PEMRSTRETCHBLT"]
old-location: gdi\emrstretchblt.htm
tech.root: gdi
ms.assetid: 957b09d2-a706-4045-affb-fd530cd4fa3a
ms.date: 12/05/2018
ms.keywords: '*PEMRSTRETCHBLT, EMRSTRETCHBLT, EMRSTRETCHBLT structure [Windows GDI], PEMRSTRETCHBLT, PEMRSTRETCHBLT structure pointer [Windows GDI], _win32_EMRSTRETCHBLT_str, gdi.emrstretchblt, wingdi/EMRSTRETCHBLT, wingdi/PEMRSTRETCHBLT'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: EMRSTRETCHBLT, *PEMRSTRETCHBLT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSTRETCHBLT
 - wingdi/tagEMRSTRETCHBLT
 - PEMRSTRETCHBLT
 - wingdi/PEMRSTRETCHBLT
 - EMRSTRETCHBLT
 - wingdi/EMRSTRETCHBLT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRSTRETCHBLT
---

# EMRSTRETCHBLT structure


## -description

The <b>EMRSTRETCHBLT</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field xDest

Logical x-coordinate of the upper-left corner of the destination rectangle.

### -field yDest

Logical y-coordinate of the upper-left corner of the destination rectangle.

### -field cxDest

Logical width of the destination rectangle.

### -field cyDest

Logical height of the destination rectangle.

### -field dwRop

Raster-operation code. These codes define how the color data of the source rectangle is to be combined with the color data of the destination rectangle to achieve the final color.

### -field xSrc

Logical x-coordinate of the upper-left corner of the source rectangle.

### -field ySrc

Logical y-coordinate of the upper-left corner of the source rectangle.

### -field xformSrc

World-space to page-space transformation of the source device context.

### -field crBkColorSrc

Background color (the RGB value) of the source device context. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field iUsageSrc

Value of the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.

### -field offBmiSrc

Offset to the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmiSrc

Size of the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBitsSrc

Offset to source bitmap bits.

### -field cbBitsSrc

Size of source bitmap bits.

### -field cxSrc

Width of the source rectangle, in logical units.

### -field cySrc

Height of the source rectangle, in logical units.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>