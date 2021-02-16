---
UID: NS:wingdi.tagEMRALPHABLEND
title: EMRALPHABLEND (wingdi.h)
description: The EMRALPHABLEND structure contains members for the AlphaBlend enhanced metafile record.
helpviewer_keywords: ["*PEMRALPHABLEND","EMRALPHABLEND","EMRALPHABLEND structure [Windows GDI]","PEMRALPHABLEND","PEMRALPHABLEND structure pointer [Windows GDI]","_win32_EMRALPHABLEND_str","gdi.emralphablend","wingdi/EMRALPHABLEND","wingdi/PEMRALPHABLEND"]
old-location: gdi\emralphablend.htm
tech.root: gdi
ms.assetid: 3270d8ed-a174-4d77-a9a7-3e3f0cab2a23
ms.date: 12/05/2018
ms.keywords: '*PEMRALPHABLEND, EMRALPHABLEND, EMRALPHABLEND structure [Windows GDI], PEMRALPHABLEND, PEMRALPHABLEND structure pointer [Windows GDI], _win32_EMRALPHABLEND_str, gdi.emralphablend, wingdi/EMRALPHABLEND, wingdi/PEMRALPHABLEND'
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
req.typenames: EMRALPHABLEND, *PEMRALPHABLEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRALPHABLEND
 - wingdi/tagEMRALPHABLEND
 - PEMRALPHABLEND
 - wingdi/PEMRALPHABLEND
 - EMRALPHABLEND
 - wingdi/EMRALPHABLEND
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
 - EMRALPHABLEND
---

# EMRALPHABLEND structure


## -description

The <b>EMRALPHABLEND</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field xDest

The x coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -field yDest

The y coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -field cxDest

Logical width of the destination rectangle.

### -field cyDest

Logical height of the destination rectangle.

### -field dwRop

Stores the <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> structure.

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

Width of source rectangle in logical units.

### -field cySrc

Height of the source rectangle in logical units.

## -remarks

This structure is to be used during metafile playback.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>