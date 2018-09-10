---
UID: NF:gdipluspath.PathGradientBrush.SetFocusScales
title: PathGradientBrush::SetFocusScales
author: windows-sdk-content
description: The PathGradientBrush::SetFocusScales method sets the focus scales of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setfocusscales.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PathGradientBrush class [GDI+],SetFocusScales method, PathGradientBrush.SetFocusScales, PathGradientBrush::SetFocusScales, SetFocusScales, SetFocusScales method [GDI+], SetFocusScales method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.SetFocusScales
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetFocusScales


## -description


The <b>PathGradientBrush::SetFocusScales</b> method sets the focus scales of this path gradient brush. 


## -parameters




### -param xScale [in]

Type: <b>REAL</b>

Real number that specifies the x focus scale. 


### -param yScale [in]

Type: <b>REAL</b>

Real number that specifies the y focus scale. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



By default, the center color of a path gradient is at the center point. By calling <b>PathGradientBrush::SetFocusScales</b>, you can specify that the center color should appear along a path that surrounds the center point. That path is the boundary path scaled by a factor of 
				<i>xScale</i> in the x direction and by a factor of 
				<i>yScale</i> in the y direction. The area inside the scaled path is filled with the center color.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The code calls the <b>PathGradientBrush::SetFocusScales</b> method of the 
						<b>PathGradientBrush</b>object to set the brush's focus scales to (0.2, 0.2). Then the code uses the path gradient brush to paint a rectangle that includes the triangular path.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetFocusScales(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {Point(100, 0), Point(200, 200), Point(0, 200)};

   // No GraphicsPath object is created. The PathGradientBrush
   // object is constructed directly from the array of points.
   PathGradientBrush pthGrBrush(points, 3);

   Color colors[] = {
      Color(255, 255, 0, 0),    // red
      Color(255, 0, 0, 255)};   // blue

   REAL relativePositions[] = {
      0.0f,    // red at the boundary of the outer triangle
      1.0f};   // blue at the boundary of the inner triangle

   pthGrBrush.SetInterpolationColors(colors, relativePositions, 2);

   // The inner triangle is formed by scaling the outer triangle
   // about its centroid. The scaling factor is 0.2 in both
   // the x and y directions.
   pthGrBrush.SetFocusScales(0.2f, 0.2f);

   // Fill a rectangle that is larger than the triangle
   // specified in the Point array. The portion of the
   // rectangle outside the triangle will not be painted.
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 200, 200); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/3f5db503-dd5a-4a33-a8c5-89817c0e3417">PathGradientBrush::GetFocusScales</a>



<a href="https://msdn.microsoft.com/91a0a611-b0c1-47b7-b030-1544128c0460">PathGradientBrush::SetInterpolationColors</a>
 

 

