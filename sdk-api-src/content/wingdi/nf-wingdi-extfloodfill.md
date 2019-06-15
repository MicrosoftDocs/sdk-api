---
UID: NF:wingdi.ExtFloodFill
title: ExtFloodFill function (wingdi.h)
author: windows-sdk-content
description: The ExtFloodFill function fills an area of the display surface with the current brush.
old-location: gdi\extfloodfill.htm
tech.root: gdi
ms.assetid: b996d47d-5aaf-4b13-8643-209744e5a04b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExtFloodFill, ExtFloodFill function [Windows GDI], FLOODFILLBORDER, FLOODFILLSURFACE, _win32_ExtFloodFill, gdi.extfloodfill, wingdi/ExtFloodFill
ms.topic: function
f1_keywords: ["wingdi/ExtFloodFill"]
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
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
 - ExtFloodFill
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExtFloodFill function


## -description


The <b>ExtFloodFill</b> function fills an area of the display surface with the current brush.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param x [in]

The x-coordinate, in logical units, of the point where filling is to start.


### -param y [in]

The y-coordinate, in logical units, of the point where filling is to start.


### -param color [in]

The color of the boundary or of the area to be filled. The interpretation of <i>crColor</i> depends on the value of the <i>fuFillType</i> parameter. To create a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.


### -param type [in]

The type of fill operation to be performed. This parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FLOODFILLBORDER"></a><a id="floodfillborder"></a><dl>
<dt><b>FLOODFILLBORDER</b></dt>
</dl>
</td>
<td width="60%">
The fill area is bounded by the color specified by the <i>crColor</i> parameter. This style is identical to the filling performed by the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-floodfill">FloodFill</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="FLOODFILLSURFACE"></a><a id="floodfillsurface"></a><dl>
<dt><b>FLOODFILLSURFACE</b></dt>
</dl>
</td>
<td width="60%">
The fill area is defined by the color that is specified by <i>crColor</i>. Filling continues outward in all directions as long as the color is encountered. This style is useful for filling areas with multicolored boundaries.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The following are some of the reasons this function might fail:

<ul>
<li>The filling could not be completed.</li>
<li>The specified point has the boundary color specified by the <i>crColor</i> parameter (if FLOODFILLBORDER was requested).</li>
<li>The specified point does not have the color specified by <i>crColor</i> (if FLOODFILLSURFACE was requested).</li>
<li>The point is outside the clipping regionthat is, it is not visible on the device.</li>
</ul>
If the <i>fuFillType</i> parameter is FLOODFILLBORDER, the system assumes that the area to be filled is completely bounded by the color specified by the <i>crColor</i> parameter. The function begins filling at the point specified by the <i>nXStart</i> and <i>nYStart</i> parameters and continues in all directions until it reaches the boundary.

If <i>fuFillType</i> is FLOODFILLSURFACE, the system assumes that the area to be filled is a single color. The function begins to fill the area at the point specified by <i>nXStart</i> and <i>nYStart</i> and continues in all directions, filling all adjacent regions containing the color specified by <i>crColor</i>.

Only memory device contexts and devices that support raster-display operations support the <b>ExtFloodFill</b> function. To determine whether a device supports this technology, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function.


#### Examples

For an example, see "Adding Lines and Graphs to a Menu" in <a href="https://docs.microsoft.com/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-floodfill">FloodFill</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

