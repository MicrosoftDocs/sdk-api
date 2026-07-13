---
UID: NF:gdipluspath.PathGradientBrush.GetBlendCount
title: PathGradientBrush::GetBlendCount (gdipluspath.h)
description: The PathGradientBrush::GetBlendCount method gets the number of blend factors currently set for this path gradient brush.
helpviewer_keywords: ["GetBlendCount","GetBlendCount method [GDI+]","GetBlendCount method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetBlendCount method","PathGradientBrush.GetBlendCount","PathGradientBrush::GetBlendCount","_gdiplus_CLASS_PathGradientBrush_GetBlendCount_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetBlendCount_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetBlendCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getblendcount_26.htm
ms.date: 12/05/2018
ms.keywords: GetBlendCount, GetBlendCount method [GDI+], GetBlendCount method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetBlendCount method, PathGradientBrush.GetBlendCount, PathGradientBrush::GetBlendCount, _gdiplus_CLASS_PathGradientBrush_GetBlendCount_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetBlendCount_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::GetBlendCount
 - gdipluspath/PathGradientBrush::GetBlendCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.GetBlendCount
---

# PathGradientBrush::GetBlendCount


## -description

The <b>PathGradientBrush::GetBlendCount</b> method gets the number of blend factors currently set for this path gradient brush.



## -returns

Type: <b>INT</b>

This method returns the number of blend factors currently set for this path gradient brush.

## -remarks

Before you call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblend">PathGradientBrush::GetBlend</a> method of a 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object, you must allocate two buffers: one to receive an array of blend factors and one to receive an array of blend positions. To determine the size of the required buffers, call the <b>PathGradientBrush::GetBlendCount</b> method of the 
				<b>PathGradientBrush</b> object. The size (in bytes) of each buffer should be the return value of <b>PathGradientBrush::GetBlendCount</b> multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example demonstrates several methods of the 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> class, including <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a>, <b>PathGradientBrush::GetBlendCount</b>, and <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblend">PathGradientBrush::GetBlend</a>. The code creates a 
						<b>PathGradientBrush</b> object and calls the <b>PathGradientBrush::SetBlend</b> method to establish a set of blend factors and blend positions for the brush. Then the code calls the <b>PathGradientBrush::GetBlendCount</b> method to retrieve the number of blend factors. After the number of blend factors is retrieved, the code allocates two buffers: one to receive the array of blend factors and one to receive the array of blend positions. Then the code calls the <b>PathGradientBrush::GetBlend</b> method to retrieve the blend factors and the blend positions.


```cpp
VOID Example_GetBlend(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

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
   graphics.FillEllipse(&pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   INT blendCount = pthGrBrush.GetBlendCount();
   REAL* factors = new REAL[blendCount];
   REAL* positions = new REAL[blendCount];

   pthGrBrush.GetBlend(factors, positions, blendCount);

   for(INT j = 0; j < blendCount; ++j)
   {
      // Inspect or use the value in factors[j].
      // Inspect or use the value in positions[j].    
   }

   delete [] factors;
   delete [] positions; 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblend">PathGradientBrush::GetBlend</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a>
