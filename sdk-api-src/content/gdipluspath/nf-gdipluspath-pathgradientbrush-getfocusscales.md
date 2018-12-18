---
UID: NF:gdipluspath.PathGradientBrush.GetFocusScales
title: PathGradientBrush::GetFocusScales
author: windows-sdk-content
description: The PathGradientBrush::GetFocusScales method gets the focus scales of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetFocusScales_xScale_yScale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getfocusscales.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFocusScales, GetFocusScales method [GDI+], GetFocusScales method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetFocusScales method, PathGradientBrush.GetFocusScales, PathGradientBrush::GetFocusScales, _gdiplus_CLASS_PathGradientBrush_GetFocusScales_xScale_yScale_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetFocusScales_xScale_yScale_
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
 - PathGradientBrush.GetFocusScales
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetFocusScales


## -description


The <b>PathGradientBrush::GetFocusScales</b> method gets the focus scales of this path gradient brush. 


## -parameters




### -param xScale [out]

Type: <b>REAL*</b>

Pointer to a 
					<b>REAL</b> that receives the x focus scale value. 


### -param yScale [out]

Type: <b>REAL*</b>

Pointer to a 
					<b>REAL</b> that receives the y focus scale value. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



By default, the center color of a path gradient is at the center point. By calling <a href="https://msdn.microsoft.com/en-us/library/ms535086(v=VS.85).aspx">PathGradientBrush::SetFocusScales</a>, you can specify that the center color should appear along a path that surrounds the center point. For example, suppose the boundary path is a triangle and the center point is at the centroid of that triangle. Also assume that the boundary color is red and the center color is blue. If you set the focus scales to (0.2, 0.2), the color is blue along the boundary of a small triangle that surrounds the center point. That small triangle is the main boundary path scaled by a factor of 0.2 in the x direction and 0.2 in the y direction. When you paint with the path gradient brush, the color will change gradually from red to blue as you move from the boundary of the large triangle to the boundary of the small triangle. The area inside the small triangle will be filled with blue.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>object based on a triangular path. The code sets the focus scales of the path gradient brush to (0.2, 0.2) and then uses the path gradient brush to fill an area that contains the triangular path. Finally, the code calls the <b>PathGradientBrush::GetFocusScales</b> method of the 
						<b>PathGradientBrush</b>object to obtain the values of the x focus scale and the y focus scale.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetFocusScales(HDC hdc)
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

   // Obtain information about the path gradient brush.
   REAL xScale = 0.0f;
   REAL yScale = 0.0f;
   pthGrBrush.GetFocusScales(&amp;xScale, &amp;yScale);

   // The value of xScale is now 0.2.
   // The value of yScale is now 0.2. 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535086(v=VS.85).aspx">PathGradientBrush::SetFocusScales</a>
 

 

