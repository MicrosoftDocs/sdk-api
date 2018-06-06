---
UID: NF:wingdi.FloodFill
title: FloodFill function
author: windows-sdk-content
description: The FloodFill function fills an area of the display surface with the current brush. The area is assumed to be bounded as specified by the crFill parameter.
old-location: gdi\floodfill.htm
old-project: gdi
ms.assetid: e53bebb5-4e46-4ea4-8d41-c12f4c6645ef
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FloodFill, FloodFill function [Windows GDI], _win32_FloodFill, gdi.floodfill, wingdi/FloodFill
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - FloodFill
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FloodFill function


## -description


The <b>FloodFill</b> function fills an area of the display surface with the current brush. The area is assumed to be bounded as specified by the <i>crFill</i> parameter.
<div class="alert"><b>Note</b>  The <b>FloodFill</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">ExtFloodFill</a> function with FLOODFILLBORDER specified.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to a device context.


### -param x

TBD


### -param y

TBD


### -param color

TBD




#### - crFill [in]

The color of the boundary or the area to be filled. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


#### - nXStart [in]

The x-coordinate, in logical units, of the point where filling is to start.


#### - nYStart [in]

The y-coordinate, in logical units, of the point where filling is to start.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The following are reasons this function might fail:

<ul>
<li>The fill could not be completed.</li>
<li>The given point has the boundary color specified by the <i>crFill</i> parameter.</li>
<li>The given point lies outside the current clipping regionthat is, it is not visible on the device.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">
        COLORREF
      </a>



<a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">
        ExtFloodFill
      </a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">
        RGB
      </a>
 

 

