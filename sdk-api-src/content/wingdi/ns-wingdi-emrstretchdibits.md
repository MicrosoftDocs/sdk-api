---
UID: NS:wingdi.tagEMRSTRETCHDIBITS
title: EMRSTRETCHDIBITS (wingdi.h)
description: The EMRSTRETCHDIBITS structure contains members for the StretchDIBits enhanced metafile record.
helpviewer_keywords: ["*PEMRSTRETCHDIBITS","EMRSTRETCHDIBITS","EMRSTRETCHDIBITS structure [Windows GDI]","PEMRSTRETCHDIBITS","PEMRSTRETCHDIBITS structure pointer [Windows GDI]","_win32_EMRSTRETCHDIBITS_str","gdi.emrstretchdibits","wingdi/EMRSTRETCHDIBITS","wingdi/PEMRSTRETCHDIBITS"]
old-location: gdi\emrstretchdibits.htm
tech.root: gdi
ms.assetid: aa104ffa-44ed-41f6-a1a7-23bbab68e16c
ms.date: 12/05/2018
ms.keywords: '*PEMRSTRETCHDIBITS, EMRSTRETCHDIBITS, EMRSTRETCHDIBITS structure [Windows GDI], PEMRSTRETCHDIBITS, PEMRSTRETCHDIBITS structure pointer [Windows GDI], _win32_EMRSTRETCHDIBITS_str, gdi.emrstretchdibits, wingdi/EMRSTRETCHDIBITS, wingdi/PEMRSTRETCHDIBITS'
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
req.typenames: EMRSTRETCHDIBITS, *PEMRSTRETCHDIBITS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSTRETCHDIBITS
 - wingdi/tagEMRSTRETCHDIBITS
 - PEMRSTRETCHDIBITS
 - wingdi/PEMRSTRETCHDIBITS
 - EMRSTRETCHDIBITS
 - wingdi/EMRSTRETCHDIBITS
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
 - EMRSTRETCHDIBITS
---

# EMRSTRETCHDIBITS structure


## -description

The <b>EMRSTRETCHDIBITS</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field xDest

Logical x-coordinate of the upper-left corner of the destination rectangle.

### -field yDest

Logical y-coordinate of the upper-left corner of the destination rectangle.

### -field xSrc

Logical x-coordinate of the upper-left corner of the source rectangle.

### -field ySrc

Logical y-coordinate of the upper-left corner of the source rectangle.

### -field cxSrc

Width of the source rectangle, in logical units.

### -field cySrc

Height of the source rectangle, in logical units.

### -field offBmiSrc

Offset to the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmiSrc

Size of the source <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBitsSrc

Offset to source bitmap bits.

### -field cbBitsSrc

Size of source bitmap bits.

### -field iUsageSrc

Value of the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.

### -field dwRop

Raster-operation code. These codes define how the color data of the source rectangle is to be combined with the color data of the destination rectangle to achieve the final color.

### -field cxDest

Logical width of the destination rectangle.

### -field cyDest

Logical height of the destination rectangle.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>