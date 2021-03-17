---
UID: NS:wingdi.tagEMRTRANSPARENTBLT
title: EMRTRANSPARENTBLT (wingdi.h)
description: The EMRTRANSPARENTBLT structure contains members for the TransparentBLT enhanced metafile record.
helpviewer_keywords: ["*PEMRTRANSPARENTBLT","EMREMRTRANSPARENTBLT","EMREMRTRANSPARENTBLT structure [Windows GDI]","EMRTRANSPARENTBLT","EMRTRANSPARENTBLT structure [Windows GDI]","PEMREMRTRANSPARENTBLT","PEMREMRTRANSPARENTBLT structure pointer [Windows GDI]","_win32_EMRTRANSPARENTBLT_str","gdi.emrtransparentblt","wingdi/EMRTRANSPARENTBLT","wingdi/PEMREMRTRANSPARENTBLT"]
old-location: gdi\emrtransparentblt.htm
tech.root: gdi
ms.assetid: f343bc6a-87b8-4c6b-b2cb-3d7f2f515fc1
ms.date: 12/05/2018
ms.keywords: '*PEMRTRANSPARENTBLT, EMREMRTRANSPARENTBLT, EMREMRTRANSPARENTBLT structure [Windows GDI], EMRTRANSPARENTBLT, EMRTRANSPARENTBLT structure [Windows GDI], PEMREMRTRANSPARENTBLT, PEMREMRTRANSPARENTBLT structure pointer [Windows GDI], _win32_EMRTRANSPARENTBLT_str, gdi.emrtransparentblt, wingdi/EMRTRANSPARENTBLT, wingdi/PEMREMRTRANSPARENTBLT'
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
req.typenames: EMRTRANSPARENTBLT, *PEMRTRANSPARENTBLT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRTRANSPARENTBLT
 - wingdi/tagEMRTRANSPARENTBLT
 - PEMRTRANSPARENTBLT
 - wingdi/PEMRTRANSPARENTBLT
 - EMRTRANSPARENTBLT
 - wingdi/EMRTRANSPARENTBLT
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
 - EMREMRTRANSPARENTBLT
---

# EMRTRANSPARENTBLT structure


## -description

The <b>EMRTRANSPARENTBLT</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">TransparentBLT</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

Inclusive bounds, in device units.

### -field xDest

Logical x coordinate of the upper-left corner of the destination rectangle.

### -field yDest

Logical y coordinate of the upper-left corner of the destination rectangle.

### -field cxDest

Logical width of the destination rectangle.

### -field cyDest

Logical height of the destination rectangle.

### -field dwRop

Stores the transparent color.

### -field xSrc

Logical x coordinate of the upper-left corner of the source rectangle.

### -field ySrc

Logical y coordinate of the upper-left corner of the source rectangle.

### -field xformSrc

World-space to page-space transformation of the source device context.

### -field crBkColorSrc

Background color (the RGB value) of the source device context. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field iUsageSrc

Source bitmap information color table usage (DIB_RGB_COLORS).

### -field offBmiSrc

Offset to the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmiSrc

Size of the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBitsSrc

Offset to the source bitmap bits.

### -field cbBitsSrc

Size of the source bitmap bits.

### -field cxSrc

Width of the source rectangle, in logical units.

### -field cySrc

Height of the source rectangle, in logical units.

## -remarks

This structure is to be used during metafile playback.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">TransparentBLT</a>