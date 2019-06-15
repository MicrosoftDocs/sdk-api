---
UID: NS:wingdi.tagEMRBITBLT
title: EMRBITBLT (wingdi.h)
author: windows-sdk-content
description: The EMRBITBLT structure contains members for the BitBlt enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.
old-location: gdi\emrbitblt.htm
tech.root: gdi
ms.assetid: ed3dbed6-4a2c-4fba-a803-f407fe60d750
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRBITBLT, EMRBITBLT, EMRBITBLT structure [Windows GDI], PEMRBITBLT, PEMRBITBLT structure pointer [Windows GDI], _win32_EMRBITBLT_str, gdi.emrbitblt, wingdi/EMRBITBLT, wingdi/PEMRBITBLT"
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
 - EMRBITBLT
product: Windows
targetos: Windows
req.typenames: EMRBITBLT, *PEMRBITBLT
req.redist: 
ms.custom: 19H1
---

# EMRBITBLT structure


## -description



The <b>EMRBITBLT</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.




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


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

