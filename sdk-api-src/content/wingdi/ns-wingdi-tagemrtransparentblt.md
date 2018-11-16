---
UID: NS:wingdi.tagEMRTRANSPARENTBLT
title: tagEMRTRANSPARENTBLT
author: windows-sdk-content
description: The EMRTRANSPARENTBLT structure contains members for the TransparentBLT enhanced metafile record.
old-location: gdi\emrtransparentblt.htm
tech.root: gdi
ms.assetid: f343bc6a-87b8-4c6b-b2cb-3d7f2f515fc1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PEMRTRANSPARENTBLT, EMREMRTRANSPARENTBLT, EMREMRTRANSPARENTBLT structure [Windows GDI], EMRTRANSPARENTBLT, EMRTRANSPARENTBLT structure [Windows GDI], PEMREMRTRANSPARENTBLT, PEMREMRTRANSPARENTBLT structure pointer [Windows GDI], _win32_EMRTRANSPARENTBLT_str, gdi.emrtransparentblt, tagEMRTRANSPARENTBLT, wingdi/EMRTRANSPARENTBLT, wingdi/PEMREMRTRANSPARENTBLT"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EMREMRTRANSPARENTBLT
product: Windows
targetos: Windows
req.typenames: EMRTRANSPARENTBLT, *PEMRTRANSPARENTBLT
req.redist: 
---

# tagEMRTRANSPARENTBLT structure


## -description



The <b>EMRTRANSPARENTBLT</b> structure contains members for the <a href="https://msdn.microsoft.com/900b2ca3-398d-4128-a1ae-8b4940574327">TransparentBLT</a> enhanced metafile record.




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

Background color (the RGB value) of the source device context. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


### -field iUsageSrc

Source bitmap information color table usage (DIB_RGB_COLORS).


### -field offBmiSrc

Offset to the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field cbBmiSrc

Size of the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


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




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/900b2ca3-398d-4128-a1ae-8b4940574327">TransparentBLT</a>
 

 

