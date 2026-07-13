---
UID: NF:gdipluspen.Pen.ResetTransform
title: Pen::ResetTransform (gdipluspen.h)
description: The Pen::ResetTransform method sets the world transformation matrix of this Pen object to the identity matrix.
helpviewer_keywords: ["Pen class [GDI+]","ResetTransform method","Pen.ResetTransform","Pen::ResetTransform","ResetTransform","ResetTransform method [GDI+]","ResetTransform method [GDI+]","Pen class","_gdiplus_CLASS_Pen_ResetTransform_","gdiplus._gdiplus_CLASS_Pen_ResetTransform_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_ResetTransform_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\resettransform_27.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],ResetTransform method, Pen.ResetTransform, Pen::ResetTransform, ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_ResetTransform_, gdiplus._gdiplus_CLASS_Pen_ResetTransform_
req.header: gdipluspen.h
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
 - Pen::ResetTransform
 - gdipluspen/Pen::ResetTransform
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
 - Pen.ResetTransform
---

# Pen::ResetTransform


## -description

The <b>Pen::ResetTransform</b> method sets the world transformation matrix of this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to the identity matrix.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Ok</b> enumeration.

## -remarks

The identity matrix represents a transformation that does nothing. If the world transformation matrix of a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object is the identity matrix, then no world transformation is applied to items drawn using that 
				<b>Pen</b> object.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets a scaling matrix to the pen, and draws a rectangle. The code then resets the transformation of the pen and draws a second rectangle.


```cpp
VOID Example_ResetTrans(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen, and set its transformation.
   Pen pen(Color(255, 0, 0, 255), 2);
   pen.ScaleTransform(8, 4);

   // Draw a rectangle with the transformed pen.
   graphics.DrawRectangle(&pen, 50, 50, 150, 100);

   pen.ResetTransform();

   // Draw a rectangle with no pen transformation.
   graphics.DrawRectangle(&pen, 250, 50, 150, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-gettransform">Pen::GetTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-multiplytransform">Pen::MultiplyTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-rotatetransform">Pen::RotateTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-scaletransform">Pen::ScaleTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-settransform">Pen::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
