---
UID: NS:wingdi.tagEMRMASKBLT
title: EMRMASKBLT (wingdi.h)
description: The EMRMASKBLT structure contains members for the MaskBlt enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.
helpviewer_keywords: ["*PEMRMASKBLT","EMRMASKBLT","EMRMASKBLT structure [Windows GDI]","PEMRMASKBLT","PEMRMASKBLT structure pointer [Windows GDI]","_win32_EMRMASKBLT_str","gdi.emrmaskblt","wingdi/EMRMASKBLT","wingdi/PEMRMASKBLT"]
old-location: gdi\emrmaskblt.htm
tech.root: gdi
ms.assetid: 4c9e8631-8b76-423f-9691-8c93c6412d41
ms.date: 12/05/2018
ms.keywords: '*PEMRMASKBLT, EMRMASKBLT, EMRMASKBLT structure [Windows GDI], PEMRMASKBLT, PEMRMASKBLT structure pointer [Windows GDI], _win32_EMRMASKBLT_str, gdi.emrmaskblt, wingdi/EMRMASKBLT, wingdi/PEMRMASKBLT'
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
req.typenames: EMRMASKBLT, *PEMRMASKBLT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRMASKBLT
 - wingdi/tagEMRMASKBLT
 - PEMRMASKBLT
 - wingdi/PEMRMASKBLT
 - EMRMASKBLT
 - wingdi/EMRMASKBLT
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
 - EMRMASKBLT
---

# EMRMASKBLT structure


## -description

The <b>EMRMASKBLT</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a> enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.

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

Value of the <b>bmiColors</b> member of the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.

### -field offBmiSrc

Offset to source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmiSrc

Size of source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBitsSrc

Offset to source bitmap bits.

### -field cbBitsSrc

Size of source bitmap bits.

### -field xMask

Horizontal pixel offset into mask bitmap.

### -field yMask

Vertical pixel offset into mask bitmap.

### -field iUsageMask

Value of the <b>bmiColors</b> member of the mask <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBmiMask

Offset to mask <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmiMask

Size of mask <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBitsMask

Offset to mask bitmap bits.

### -field cbBitsMask

Size of mask bitmap bits.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>