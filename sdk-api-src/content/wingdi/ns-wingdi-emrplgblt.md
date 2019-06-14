---
UID: NS:wingdi.tagEMRPLGBLT
title: EMRPLGBLT (wingdi.h)
author: windows-sdk-content
description: The EMRPLGBLT structure contains members for the PlgBlt enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.
old-location: gdi\emrplgblt.htm
tech.root: gdi
ms.assetid: c802baa8-2f11-46e1-948c-f63c40e94266
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRPLGBLT, EMRPLGBLT, EMRPLGBLT structure [Windows GDI], PEMRPLGBLT, PEMRPLGBLT structure pointer [Windows GDI], _win32_EMRPLGBLT_str, gdi.emrplgblt, wingdi/EMRPLGBLT, wingdi/PEMRPLGBLT"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRPLGBLT
product: Windows
targetos: Windows
req.typenames: EMRPLGBLT, *PEMRPLGBLT
req.redist: 
ms.custom: 19H1
---

# EMRPLGBLT structure


## -description



The <b>EMRPLGBLT</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a> enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field aptlDest

Array of three points in logical space that identify three corners of the destination parallelogram. The upper-left corner of the source rectangle is mapped to the first point in this array, the upper-right corner to the second point in this array, and the lower-left corner to the third point. The lower-right corner of the source rectangle is mapped to the implicit fourth point in the parallelogram.


### -field xSrc

Logical x-coordinate of the upper-left corner of the source rectangle.


### -field ySrc

Logical y-coordinate of the upper-left corner of the source rectangle.


### -field cxSrc

Logical width of the source.


### -field cySrc

Logical height of the source.


### -field xformSrc

World-space to page-space transformation of the source device context.


### -field crBkColorSrc

Background color (the RGB value) of the source device context. To make a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.


### -field iUsageSrc

Value of the <b>bmiColors</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.


### -field offBmiSrc

Offset to source <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure.


### -field cbBmiSrc

Size of source <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure.


### -field offBitsSrc

Offset to source bitmap bits.


### -field cbBitsSrc

Size of source bitmap bits.


### -field xMask

Horizontal pixel offset into mask bitmap.


### -field yMask

Vertical pixel offset into mask bitmap.


### -field iUsageMask

Value of the <b>bmiColors</b> member of the mask <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure.


### -field offBmiMask

Offset to mask <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure.


### -field cbBmiMask

Size of mask <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure.


### -field offBitsMask

Offset to mask bitmap bits.


### -field cbBitsMask

Size of mask bitmap bits.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

