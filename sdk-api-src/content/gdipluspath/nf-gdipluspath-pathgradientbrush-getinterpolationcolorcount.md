---
UID: NF:gdipluspath.PathGradientBrush.GetInterpolationColorCount
title: PathGradientBrush::GetInterpolationColorCount
author: windows-sdk-content
description: The PathGradientBrush::GetInterpolationColorCount method gets the number of preset colors currently specified for this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getinterpolationcolorcount_80.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetInterpolationColorCount, GetInterpolationColorCount method [GDI+], GetInterpolationColorCount method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetInterpolationColorCount method, PathGradientBrush.GetInterpolationColorCount, PathGradientBrush::GetInterpolationColorCount, _gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_
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
 - PathGradientBrush.GetInterpolationColorCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetInterpolationColorCount


## -description


The <b>PathGradientBrush::GetInterpolationColorCount</b> method gets the number of preset colors currently specified for this path gradient brush.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of preset colors currently specified for this path gradient brush.




## -remarks



A simple path gradient brush has two colors: a boundary color and a center color. When you paint with such a brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point. You can create a more complex gradient by specifying an array of preset colors and an array of blend positions.

You can obtain the interpolation colors and interpolation positions currently set for a 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object by calling the <a href="https://msdn.microsoft.com/ed0e89c7-a523-407e-a800-742bc8dec886">PathGradientBrush::GetInterpolationColors</a> method of that 
				<b>PathGradientBrush</b>object. Before you call the <b>PathGradientBrush::GetInterpolationColors</b> method, you must allocate two buffers: one to hold the array of interpolation colors and one to hold the array of interpolation positions. You can call the <b>PathGradientBrush::GetInterpolationColorCount</b> method of the 
				<b>PathGradientBrush</b>object to determine the required size of those buffers. The size of the color buffer is the return value of <b>GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>). The size of the position buffer is the value of <b>PathGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object from a triangular path. The code sets the preset colors to red, blue, and aqua and sets the blend positions to 0, 0.6, and 1. The code calls the <b>PathGradientBrush::GetInterpolationColorCount</b> method of the 
						<b>PathGradientBrush</b>object to obtain the number of preset colors currently set for the brush. Next, the code allocates two buffers: one to hold the array of preset colors, and one to hold the array of blend positions. The call to the <a href="https://msdn.microsoft.com/ed0e89c7-a523-407e-a800-742bc8dec886">PathGradientBrush::GetInterpolationColors</a> method of the 
						<b>PathGradientBrush</b>object fills the buffers with the preset colors and the blend positions. Finally the code fills a small square with each of the preset colors.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetInterpColors(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush from an array of points, and
   // set the interpolation colors for that brush.

   Point points[] = {Point(100, 0), Point(200, 200), Point(0, 200)};
   PathGradientBrush pthGrBrush(points, 3);

   Color col[] = {
      Color(255, 255, 0, 0),     // red
      Color(255, 0, 0, 255),     // blue
      Color(255, 0, 255, 255)};  // aqua

   REAL pos[] = {
      0.0f,    // red at the boundary
      0.6f,    // blue 60 percent of the way from the boundary to the center
      1.0f};   // aqua at the center

   pthGrBrush.SetInterpolationColors(col, pos, 3);

   // Obtain information about the path gradient brush.
   INT colorCount = pthGrBrush.GetInterpolationColorCount();
   Color* colors = new Color[colorCount];
   REAL* positions = new REAL[colorCount];
   pthGrBrush.GetInterpolationColors(colors, positions, colorCount);

   // Fill a small square with each of the interpolation colors.
   SolidBrush solidBrush(Color(255, 255, 255, 255));

   for(INT j = 0; j &lt; colorCount; ++j)
   {
      solidBrush.SetColor(colors[j]);
      graphics.FillRectangle(&amp;solidBrush, 15*j, 0, 10, 10);
   }

   delete [] colors;
   delete [] positions; 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/ed0e89c7-a523-407e-a800-742bc8dec886">PathGradientBrush::GetInterpolationColors</a>



<a href="https://msdn.microsoft.com/91a0a611-b0c1-47b7-b030-1544128c0460">PathGradientBrush::SetInterpolationColors</a>
 

 

