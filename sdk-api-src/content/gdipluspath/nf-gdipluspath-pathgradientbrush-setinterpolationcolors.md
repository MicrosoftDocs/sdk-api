---
UID: NF:gdipluspath.PathGradientBrush.SetInterpolationColors
title: PathGradientBrush::SetInterpolationColors
author: windows-sdk-content
description: The PathGradientBrush::SetInterpolationColors method sets the preset colors and the blend positions of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setinterpolationcolors_29presetcolors_blendpositions_count.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PathGradientBrush class [GDI+],SetInterpolationColors method, PathGradientBrush.SetInterpolationColors, PathGradientBrush::SetInterpolationColors, SetInterpolationColors, SetInterpolationColors method [GDI+], SetInterpolationColors method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.SetInterpolationColors
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetInterpolationColors


## -description


The <b>PathGradientBrush::SetInterpolationColors</b> method sets the preset colors and the blend positions of this path gradient brush.


## -parameters




### -param presetColors [in]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> objects that specifies the interpolation colors for the gradient. A color of a given index in the 
					<i>presetColors</i> array corresponds to the blend position of that same index in the 
					<i>blendPositions</i> array. 


### -param blendPositions [in]

Type: <b>REAL*</b>

Pointer to an array that specifies the blend positions. Each blend position is a number from 0 through 1, where 0 indicates the boundary of the gradient and 1 indicates the center point. A blend position between 0 and 1 specifies the set of all points that are a certain fraction of the distance from the boundary to the center point. For example, a blend position of 0.7 specifies the set of all points that are 70 percent of the way from the boundary to the center point. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> objects in the 
					<i>presetColors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A simple path gradient brush has two colors: a boundary color and a center color. When you paint with such a brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point. You can create a more complex gradient by specifying an array of preset colors and an array of blend positions.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The 
						<b>PathGradientBrush::SetInterpolationColors</b> method sets the brush's preset colors to red, blue, and aqua and sets the blend positions to 0, 0, 4, and 1. The 
						<a href="https://msdn.microsoft.com/91d3fc66-4c0d-4b44-beae-59f13b80483d">Graphics::FillRectangle</a> method uses the path gradient brush to paint a rectangle that contains the triangular path.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetInterpColors(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {Point(100, 0), Point(200, 200), Point(0, 200)};
   PathGradientBrush pthGrBrush(points, 3);

   Color col[] = {
      Color(255, 255, 0, 0),     // red
      Color(255, 0, 0, 255),     // blue
      Color(255, 0, 255, 255)};  // aqua

   REAL pos[] = {
      0.0f,    // red at the boundary
      0.4f,    // blue 40 percent of the way from the boundary to the center
      1.0f};   // aqua at the center

   pthGrBrush.SetInterpolationColors(col, pos, 3);
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 300, 300);  
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
 

 

