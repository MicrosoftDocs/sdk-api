---
UID: NF:gdipluspath.PathGradientBrush.SetWrapMode
title: PathGradientBrush::SetWrapMode
author: windows-sdk-content
description: The PathGradientBrush::SetWrapMode method sets the wrap mode of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setwrapmode_12wrapmode.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PathGradientBrush class [GDI+],SetWrapMode method, PathGradientBrush.SetWrapMode, PathGradientBrush::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_
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
 - PathGradientBrush.SetWrapMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetWrapMode


## -description


The <b>PathGradientBrush::SetWrapMode</b> method sets the wrap mode of this path gradient brush.


## -parameters




### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapModeClamp</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The bounding rectangle of a path gradient brush is the smallest rectangle that encloses the brush's boundary path. When you paint the bounding rectangle with the path gradient brush, only the area inside the boundary path gets filled. The area inside the bounding rectangle but outside the boundary path does not get filled.


<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapModeClamp</a> (the default wrap mode) indicates that no painting occurs outside of the brush's bounding rectangle. All of the other wrap modes indicate that areas outside the brush's bounding rectangle will be tiled. Each tile is a copy (possibly flipped) of the filled path inside its bounding rectangle.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The code calls the <b>PathGradientBrush::SetWrapMode</b> method of the 
						<b>PathGradientBrush</b>object to set the brush's wrap mode to <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapModeTileFlipX</a>. The 
						<a href="https://msdn.microsoft.com/91d3fc66-4c0d-4b44-beae-59f13b80483d">Graphics::FillRectangle</a> method uses the path gradient brush to tile a large area. 

The output of the code is a grid of tiles. As you move from one tile to the next in a given row, the image (filled boundary path inside the bounding rectangle) is flipped horizontally.


```cpp
VOID Example_SetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(0, 0), 
      Point(100, 0), 
      Point(100, 100)};

   Color colors[] = {
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255),   // blue
      Color(255, 0, 255, 0)};  // green

   INT count = 3;

   PathGradientBrush pthGrBrush(points, 3);
   pthGrBrush.SetSurroundColors(colors, &count);
   pthGrBrush.SetWrapMode(WrapModeTileFlipX);

   graphics.FillRectangle(&pthGrBrush, 0, 0, 800, 800); 
}
```





## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/f8439574-b536-4597-8c0f-f31dcf3b3d67">PathGradientBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/03217354-391b-4103-a5b4-d151c49654e5">PathGradientBrush::SetWrapMode</a>
 

 

