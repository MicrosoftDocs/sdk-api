---
UID: NF:gdiplusgraphics.Graphics.TranslateTransform
title: Graphics::TranslateTransform (gdiplusgraphics.h)
description: The Graphics::TranslateTransform method updates this Graphics object's world transformation matrix with the product of itself and a translation matrix.
helpviewer_keywords: ["Graphics class [GDI+]","TranslateTransform method","Graphics.TranslateTransform","Graphics::TranslateTransform","TranslateTransform","TranslateTransform method [GDI+]","TranslateTransform method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_","gdiplus._gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\translatetransform.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],TranslateTransform method, Graphics.TranslateTransform, Graphics::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_
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
 - Graphics::TranslateTransform
 - gdiplusgraphics/Graphics::TranslateTransform
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
 - Graphics.TranslateTransform
---

# Graphics::TranslateTransform


## -description

The <b>Graphics::TranslateTransform</b> method updates this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object's world transformation matrix with the product of itself and a translation matrix.

## -parameters

### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal component of the translation.

### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the vertical component of the translation.

### -param order [in, optional]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the translation matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the translation matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

<div class="alert"><b>Note</b>  GDI+ handles brushes differently when the world transform scale is less than 100%(1.0f) in either the x or y direction.  If the world transform scale is less than 100%(1.0f), be sure to multiply the offset for TranslateTransform by the world transform scale.</div>
<div> </div>

#### Examples



The following example sets the world transformation of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a rotation. The call to <b>Graphics::TranslateTransform</b> multiplies the <b>Graphics</b> object's existing world transformation matrix (rotation) by a translation matrix. The MatrixOrderAppend argument specifies that the multiplication is done with the translation matrix on the right. At that point, the world transformation matrix of the <b>Graphics</b> object represents a composite transformation: first rotate, then translate. The call to <b>DrawEllipse</b> draws a rotated and translated ellipse.


```cpp
VOID Example_TranslateTransform(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   graphics.RotateTransform(30.0f);
   graphics.TranslateTransform(100.0f, 50.0f, MatrixOrderAppend);
   graphics.DrawEllipse(&pen, 0, 0, 200, 80);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettransform">Graphics::GetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resettransform">Graphics::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform">Graphics::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform">Graphics::SetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-transformpoints(incoordinatespace_incoordinatespace_inoutpoint_inint)">Graphics::TransformPoints</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>