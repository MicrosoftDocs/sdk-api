---
UID: NF:gdiplusgraphics.Graphics.ResetTransform
title: Graphics::ResetTransform (gdiplusgraphics.h)
description: The Graphics::ResetTransform method sets the world transformation matrix of this Graphics object to the identity matrix.
helpviewer_keywords: ["Graphics class [GDI+]","ResetTransform method","Graphics.ResetTransform","Graphics::ResetTransform","ResetTransform","ResetTransform method [GDI+]","ResetTransform method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_ResetTransform_","gdiplus._gdiplus_CLASS_Graphics_ResetTransform_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_ResetTransform_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\resettransform.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],ResetTransform method, Graphics.ResetTransform, Graphics::ResetTransform, ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ResetTransform_, gdiplus._gdiplus_CLASS_Graphics_ResetTransform_
req.header: gdiplusgraphics.h
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
 - Graphics::ResetTransform
 - gdiplusgraphics/Graphics::ResetTransform
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
 - Graphics.ResetTransform
---

# Graphics::ResetTransform


## -description

The <b>Graphics::ResetTransform</b> method sets the world transformation matrix of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to the identity matrix.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The identity matrix represents a transformation that does nothing. If the world transformation matrix of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is the identity matrix, then no world transformation is applied to items drawn by that <b>Graphics</b> object.


#### Examples



The following example sets the world transformation of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a 45-degree rotation and then draws a rectangle. The code calls the <b>ResetTransform</b> method of the <b>Graphics</b> object and then draws a second rectangle. No rotation transformation is applied to the second rectangle.


```cpp
VOID Example_ResetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Rotate the transformation and draw a rectangle.
   graphics.RotateTransform(45.0f);
   Pen blackPen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&blackPen, 100, 0, 100, 50);

   // Reset the transformation to identity, and draw a second rectangle.
   graphics.ResetTransform();
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&redPen, 110, 0, 100, 50);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettransform">Graphics::GetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform">Graphics::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform">Graphics::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform">Graphics::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform">Graphics::SetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-transformpoints(incoordinatespace_incoordinatespace_inoutpoint_inint)">Graphics::TransformPoints</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform">Graphics::TranslateTransform</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
