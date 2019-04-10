---
UID: NS:wingdi.tagLOGPEN
title: LOGPEN (wingdi.h)
author: windows-sdk-content
description: The LOGPEN structure defines the style, width, and color of a pen. The CreatePenIndirect function uses the LOGPEN structure.
old-location: gdi\logpen.htm
tech.root: gdi
ms.assetid: 0e098b5a-e249-43ad-a6d8-2509b6562453
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLOGPEN, *NPLOGPEN, *PLOGPEN, LOGPEN, LOGPEN structure [Windows GDI], PLOGPEN, PLOGPEN structure pointer [Windows GDI], _win32_LOGPEN_str, gdi.logpen, wingdi/LOGPEN, wingdi/PLOGPEN"
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
 - LOGPEN
product: Windows
targetos: Windows
req.typenames: LOGPEN, *PLOGPEN, *NPLOGPEN, *LPLOGPEN
req.redist: 
---

# LOGPEN structure


## -description



The <b>LOGPEN</b> structure defines the style, width, and color of a pen. The <a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a> function uses the <b>LOGPEN</b> structure.




## -struct-fields




### -field lopnStyle

The pen style, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_SOLID</td>
<td>The pen is solid.</td>
</tr>
<tr>
<td>PS_DASH</td>
<td>The pen is dashed.</td>
</tr>
<tr>
<td>PS_DOT</td>
<td>The pen is dotted.</td>
</tr>
<tr>
<td>PS_DASHDOT</td>
<td>The pen has alternating dashes and dots.</td>
</tr>
<tr>
<td>PS_DASHDOTDOT</td>
<td>The pen has dashes and double dots.</td>
</tr>
<tr>
<td>PS_NULL</td>
<td>The pen is invisible.</td>
</tr>
<tr>
<td>PS_INSIDEFRAME</td>
<td>The pen is solid. When this pen is used in any GDI drawing function that takes a bounding rectangle, the dimensions of the figure are shrunk so that it fits entirely in the bounding rectangle, taking into account the width of the pen. This applies only to geometric pens.</td>
</tr>
</table>
 


### -field lopnWidth

The <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the pen width, in logical units. If the <b>pointer</b> member is <b>NULL</b>, the pen is one pixel wide on raster devices. The <b>y</b> member in the <b>POINT</b> structure for <b>lopnWidth</b> is not used.


### -field lopnColor

The pen color. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -remarks



If the width of the pen is greater than 1 and the pen style is PS_INSIDEFRAME, the line is drawn inside the frame of all GDI objects except polygons and polylines. If the pen color does not match an available RGB value, the pen is drawn with a logical (dithered) color. If the pen width is less than or equal to 1, the PS_INSIDEFRAME style is identical to the PS_SOLID style.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/dcc65b2d-958a-4681-962f-a94895f0f243">Pen Structures</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

