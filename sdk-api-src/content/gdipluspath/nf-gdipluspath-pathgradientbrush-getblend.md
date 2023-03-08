---
UID: NF:gdipluspath.PathGradientBrush.GetBlend
title: PathGradientBrush::GetBlend (gdipluspath.h)
description: The PathGradientBrush::GetBlend method gets the blend factors and the corresponding blend positions currently set for this path gradient brush.
helpviewer_keywords: ["GetBlend","GetBlend method [GDI+]","GetBlend method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetBlend method","PathGradientBrush.GetBlend","PathGradientBrush::GetBlend","_gdiplus_CLASS_PathGradientBrush_GetBlend_blendFactors_blendPositions_count_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetBlend_blendFactors_blendPositions_count_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetBlend_blendFactors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getblend_22blendfactors_blendpositions_count.htm
ms.date: 12/05/2018
ms.keywords: GetBlend, GetBlend method [GDI+], GetBlend method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetBlend method, PathGradientBrush.GetBlend, PathGradientBrush::GetBlend, _gdiplus_CLASS_PathGradientBrush_GetBlend_blendFactors_blendPositions_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetBlend_blendFactors_blendPositions_count_
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
 - PathGradientBrush::GetBlend
 - gdipluspath/PathGradientBrush::GetBlend
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
 - PathGradientBrush.GetBlend
---

# PathGradientBrush::GetBlend


## -description

The <b>PathGradientBrush::GetBlend</b> method gets the blend factors and the corresponding blend positions currently set for this path gradient brush.

## -parameters

### -param blendFactors [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend factors.

### -param blendPositions [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend positions.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of blend factors to retrieve. Before calling the <b>PathGradientBrush::GetBlend</b> method of a 
					<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object, call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblendcount">PathGradientBrush::GetBlendCount</a> method of that same 
					<b>PathGradientBrush</b> object to determine the current number of blend factors. The number of blend positions retrieved is the same as the number of blend factors retrieved.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object has a boundary path and a center point. When you fill an area with a path gradient brush, the color changes gradually as you move from the boundary path to the center point. By default, the color is linearly related to the distance, but you can customize the relationship between color and distance by calling the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a> method.


#### Examples



The following example demonstrates several methods of the 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> class including <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a>, <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblendcount">PathGradientBrush::GetBlendCount</a>, and <b>PathGradientBrush::GetBlend</b>. The code creates a 
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



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblendcount">PathGradientBrush::GetBlendCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">PathGradientBrush::SetCenterPoint Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors">PathGradientBrush::SetSurroundColors</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>