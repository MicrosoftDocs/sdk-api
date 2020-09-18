---
UID: NF:gdiplusbrush.LinearGradientBrush.SetTransform
title: LinearGradientBrush::SetTransform (gdiplusbrush.h)
description: The LinearGradientBrush::SetTransform method sets the transformation matrix of this linear gradient brush.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetTransform method","LinearGradientBrush.SetTransform","LinearGradientBrush::SetTransform","SetTransform","SetTransform method [GDI+]","SetTransform method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\settransform_65matrix.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetTransform method, LinearGradientBrush.SetTransform, LinearGradientBrush::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_
req.header: gdiplusbrush.h
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
 - LinearGradientBrush::SetTransform
 - gdiplusbrush/LinearGradientBrush::SetTransform
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
 - LinearGradientBrush.SetTransform
---

# LinearGradientBrush::SetTransform


## -description

The <b>LinearGradientBrush::SetTransform</b> method sets the transformation matrix of this linear gradient brush.

## -parameters

### -param matrix [in]

Type: <b>const Matrix*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation matrix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object has a rectangle that specifies the starting and ending boundaries of the gradient and a mode or angle that affects the direction. If the brush's transformation matrix is set to represent any transformation other than the identity, then the boundaries and direction are transformed according to that matrix during rendering.

The transformation applies only during rendering. The boundaries stored by the 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object are not altered by the <b>LinearGradientBrush::SetTransform</b> method.


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's transformation matrix and fills a rectangle with the transformed brush.


```cpp
VOID Example_SetTransform(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush( 
      Rect(0, 0, 100, 50),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   Matrix matrix(2.0, 0, 0, 1, 0, 0);  // horizontal doubling

   // Fill a large area with the linear gradient brush (no transformation).
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 800, 50);

   linGrBrush.SetTransform(&matrix);

   // Fill a large area with the transformed linear gradient brush.
   myGraphics.FillRectangle(&linGrBrush, 0, 75, 800, 50);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-shapes-with-a-gradient-brush-use">Filling Shapes with a Gradient Brush</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-gettransform">LinearGradientBrush::GetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-resettransform">LinearGradientBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>