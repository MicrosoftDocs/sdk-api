---
UID: NF:gdipluspath.PathGradientBrush.SetTransform
title: PathGradientBrush::SetTransform (gdipluspath.h)
description: The PathGradientBrush::SetTransform method sets the transformation matrix of this path gradient brush.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetTransform method","PathGradientBrush.SetTransform","PathGradientBrush::SetTransform","SetTransform","SetTransform method [GDI+]","SetTransform method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\settransform_69matrix.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetTransform method, PathGradientBrush.SetTransform, PathGradientBrush::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_
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
 - PathGradientBrush::SetTransform
 - gdipluspath/PathGradientBrush::SetTransform
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
 - PathGradientBrush.SetTransform
---

# PathGradientBrush::SetTransform


## -description

The <b>PathGradientBrush::SetTransform</b> method sets the transformation matrix of this path gradient brush.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a 
					<b>Matrix</b> object that specifies the transformation matrix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object has a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that serves as the boundary path for the brush. When you paint with a path gradient brush, only the area inside the boundary path is filled. If the brush's transformation matrix is set to represent any transformation other than the identity, then the boundary path is transformed according to that matrix during rendering, and only the area inside the transformed path is filled.

The transformation applies only during rendering. The boundary path stored by the 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object is not altered by the <b>PathGradientBrush::SetTransform</b> method.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The 
						<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">Graphics::FillRectangle</a> method uses the path gradient brush to paint a rectangle that contains the triangular path. Next, the code creates a 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that represents a composite transformation (rotate, then translate) and passes the address of that 
						<b>Matrix</b> object to the <b>PathGradientBrush::SetTransform</b> method of the 
						<b>PathGradientBrush</b> object. The code calls 
						<a href="/previous-versions/ms535957(v=vs.85)">FillRectangle</a> a second time to paint the same rectangle using the transformed path gradient brush.


```cpp
VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Point pts[] = {
      Point(0, 0), 
      Point(100, 0), 
      Point(100, 100)};

   Color cols[] = {
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 255, 0),  // green
      Color(255, 0, 0, 0)};   // black

   INT count = 3;
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.SetSurroundColors(cols, &count);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);

   // Set the transformation for the brush (rotate, then translate).
   Matrix matrix(0.0f, 1.0f, -1.0f, 0.0f, 150.0f, 60.0f);
   pthGrBrush.SetTransform(&matrix);
   
   // Fill the same area with the transformed path gradient brush.
   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-gettransform">PathGradientBrush::GetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-multiplytransform">PathGradientBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-resettransform">PathGradientBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-rotatetransform">PathGradientBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a>