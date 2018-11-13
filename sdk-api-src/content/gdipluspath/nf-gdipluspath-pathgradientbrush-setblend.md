---
UID: NF:gdipluspath.PathGradientBrush.SetBlend
title: PathGradientBrush::SetBlend
author: windows-sdk-content
description: The PathGradientBrush::SetBlend method sets the blend factors and the blend positions of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetBlend_blendFactors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setblend_56blendfactors_blendpositions_count.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PathGradientBrush class [GDI+],SetBlend method, PathGradientBrush.SetBlend, PathGradientBrush::SetBlend, SetBlend, SetBlend method [GDI+], SetBlend method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetBlend_blendFactors_blendPositions_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetBlend_blendFactors_blendPositions_count_
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
 - PathGradientBrush.SetBlend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetBlend


## -description


The <b>PathGradientBrush::SetBlend</b> method sets the blend factors and the blend positions of this path gradient brush.


## -parameters




### -param blendFactors [in]

Type: <b>REAL*</b>

Pointer to an array of blend factors. Each number in the array should be in the range 0 through 1. 


### -param blendPositions [in]

Type: <b>REAL*</b>

Pointer to an array of blend positions. Each number in the array should be in the range 0 through 1. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>blendFactors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object has a boundary path and a center point. When you fill an area with a path gradient brush, the color changes gradually as you move from the boundary path to the center point. By default, the color is linearly related to the distance, but you can customize the relationship between color and distance by calling the <b>PathGradientBrush::SetBlend</b> method.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on an ellipse. The code calls the <b>PathGradientBrush::SetBlend</b> method of the 
						<b>PathGradientBrush</b>object to establish a set of blend factors and blend positions for the brush. Then the code uses the path gradient brush to fill the ellipse.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetBlend(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&amp;path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &amp;count);

   // Set blend factors and positions for the path gradient brush.
   REAL fac[] = {
      0.0f, 
      0.4f,     // 40 percent of the way from aqua to blue
      0.8f,     // 80 percent of the way from aqua to blue
      1.0f};

   REAL pos[] = {
      0.0f, 
      0.3f,   // 30 percent of the way from the boundary to the center
      0.7f,   // 70 percent of the way from the boundary to the center
      1.0f};

   pthGrBrush.SetBlend(fac, pos, 4);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&amp;pthGrBrush, 0, 0, 200, 100);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/8a4ff6de-615e-4128-9e88-337ed6f4af7f">PathGradientBrush::GetBlend</a>



<a href="https://msdn.microsoft.com/c87dbdab-68ea-4fac-9d37-1a12dfcf5335">PathGradientBrush::GetBlendCount</a>
 

 

