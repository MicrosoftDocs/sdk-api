---
UID: NF:gdipluspen.Pen.TranslateTransform
title: Pen::TranslateTransform (gdipluspen.h)
description: The Pen::TranslateTransform method sets the Pen object's world transformation matrix equal to the product of itself and a scaling matrix.
helpviewer_keywords: ["Pen class [GDI+]","TranslateTransform method","Pen.TranslateTransform","Pen::TranslateTransform","TranslateTransform","TranslateTransform method [GDI+]","TranslateTransform method [GDI+]","Pen class","_gdiplus_CLASS_Pen_TranslateTransform_dx_dy_order_","gdiplus._gdiplus_CLASS_Pen_TranslateTransform_dx_dy_order_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_TranslateTransform_dx_dy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\TranslateTransform_26dx_dy_order.htm
ms.date: 10/12/2022
ms.keywords: Pen class [GDI+],TranslateTransform method, Pen.TranslateTransform, Pen::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_Pen_TranslateTransform_dx_dy_order_
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
 - Pen::TranslateTransform
 - gdipluspen/Pen::TranslateTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbdyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.TranslateTransform
---

# Pen::TranslateTransform


## -description

The <b>Pen::TranslateTransform</b> method sets the 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object's world transformation matrix equal to the product of itself and a scaling matrix.

## -parameters

### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal scaling factor in the scaling matrix.

### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the vertical scaling factor in the scaling matrix.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the scaling matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the scaling matrix is on the right. The default value is <b>MatrixOrderPrepend</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate systems and transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-gettransform">Pen::GetTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-multiplytransform">Pen::MultiplyTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-resettransform">Pen::ResetTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-settransform">Pen::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
