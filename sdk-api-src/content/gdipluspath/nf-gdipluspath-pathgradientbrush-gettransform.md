---
UID: NF:gdipluspath.PathGradientBrush.GetTransform
title: PathGradientBrush::GetTransform (gdipluspath.h)
description: The PathGradientBrush::GetTransform method gets transformation matrix of this path gradient brush.
helpviewer_keywords: ["GetTransform","GetTransform method [GDI+]","GetTransform method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetTransform method","PathGradientBrush.GetTransform","PathGradientBrush::GetTransform","_gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\gettransform_69matrix.htm
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetTransform method, PathGradientBrush.GetTransform, PathGradientBrush::GetTransform, _gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_
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
 - PathGradientBrush::GetTransform
 - gdipluspath/PathGradientBrush::GetTransform
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
 - PathGradientBrush.GetTransform
---

# PathGradientBrush::GetTransform


## -description

The <b>PathGradientBrush::GetTransform</b> method gets transformation matrix of this path gradient brush.

## -parameters

### -param matrix [out]

Type: <b><a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that receives the transformation matrix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object maintains a transformation matrix that can store any affine transformation. When you use a path gradient brush to fill an area, GDI+ transforms the brush's boundary path according to the brush's transformation matrix and then fills the interior of the transformed path. The transformed path exists only during rendering; the boundary path stored in 
						<b>PathGradientBrush</b> object is not transformed.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on an array of three points. The 
						<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a> and 
						<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a> methods set the elements of the brush's transformation matrix so that the matrix represents a composite transformation (first scale, then translate). That composite transformation applies to the brush's boundary path, so the call to 
						<a href="/previous-versions/ms535957(v=vs.85)">FillRectangle</a> fills the interior of a triangle that is the result of scaling and translating the boundary path. The code calls the <b>PathGradientBrush::GetTransform</b> method of the 
						<b>PathGradientBrush</b> object to obtain the brush's transformation matrix and then calls the 
						<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-getelements">GetElements</a> method of the retrieved <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object to fill an array with the matrix elements.


```cpp
VOID Example_GetTransform(HDC hdc)
{
  Graphics graphics(hdc);

   // Create a path gradient brush and set its transformation.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.ScaleTransform(3.0f, 1.0f);
   pthGrBrush.TranslateTransform(10.0f, 30.0f, MatrixOrderAppend);

   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);

   // Obtain information about the path gradient brush.
   Matrix matrix;
   REAL elements[6];

   pthGrBrush.GetTransform(&matrix);
   matrix.GetElements(elements);

   for(INT j = 0; j <= 5; ++j)
   {
      // Inspect or use the value in elements[j].
   } 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-settransform">PathGradientBrush::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>