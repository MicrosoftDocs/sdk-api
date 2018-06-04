---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ExtFloodFill function


## -description


The <b>ExtFloodFill</b> function fills an area of the display surface with the current brush.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param x

TBD


### -param y

TBD


### -param color

TBD


### -param type

TBD




#### - crColor [in]

The color of the boundary or of the area to be filled. The interpretation of <i>crColor</i> depends on the value of the <i>fuFillType</i> parameter. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


#### - fuFillType [in]

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
The fill area is bounded by the color specified by the <i>crColor</i> parameter. This style is identical to the filling performed by the <a href="https://msdn.microsoft.com/e53bebb5-4e46-4ea4-8d41-c12f4c6645ef">FloodFill</a> function.

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
 


#### - nXStart [in]

The x-coordinate, in logical units, of the point where filling is to start.


#### - nYStart [in]

The y-coordinate, in logical units, of the point where filling is to start.


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

Only memory device contexts and devices that support raster-display operations support the <b>ExtFloodFill</b> function. To determine whether a device supports this technology, use the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function.


#### Examples

For an example, see "Adding Lines and Graphs to a Menu" in <a href="_win32_Using_Menus_cpp">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/e53bebb5-4e46-4ea4-8d41-c12f4c6645ef">FloodFill</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

