---
UID: NS:wingdi.tagEMRSTRETCHBLT
title: tagEMRSTRETCHBLT
author: windows-sdk-content
description: The EMRSTRETCHBLT structure contains members for the StretchBlt enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.
old-location: gdi\emrstretchblt.htm
old-project: gdi
ms.assetid: 957b09d2-a706-4045-affb-fd530cd4fa3a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PEMRSTRETCHBLT, EMRSTRETCHBLT, EMRSTRETCHBLT structure [Windows GDI], PEMRSTRETCHBLT, PEMRSTRETCHBLT structure pointer [Windows GDI], _win32_EMRSTRETCHBLT_str, gdi.emrstretchblt, tagEMRSTRETCHBLT, wingdi/EMRSTRETCHBLT, wingdi/PEMRSTRETCHBLT"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EMRSTRETCHBLT, *PEMRSTRETCHBLT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRSTRETCHBLT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRSTRETCHBLT structure


## -description



The <b>EMRSTRETCHBLT</b> structure contains members for the <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> enhanced metafile record. Note that graphics device interface (GDI) converts the device-dependent bitmap into a device-independent bitmap (DIB) before storing it in the metafile record.




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

Background color (the RGB value) of the source device context. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


### -field iUsageSrc

Value of the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.


### -field offBmiSrc

Offset to the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field cbBmiSrc

Size of the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field offBitsSrc

Offset to source bitmap bits.


### -field cbBitsSrc

Size of source bitmap bits.


### -field cxSrc

Width of the source rectangle, in logical units.


### -field cySrc

Height of the source rectangle, in logical units.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>
 

 

