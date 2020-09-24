---
UID: NF:gdipluspen.Pen.RotateTransform
title: Pen::RotateTransform (gdipluspen.h)
description: The Pen::RotateTransform method updates the world transformation matrix of this Pen object with the product of itself and a rotation matrix.
helpviewer_keywords: ["Pen class [GDI+]","RotateTransform method","Pen.RotateTransform","Pen::RotateTransform","RotateTransform","RotateTransform method [GDI+]","RotateTransform method [GDI+]","Pen class","_gdiplus_CLASS_Pen_RotateTransform_angle_order_","gdiplus._gdiplus_CLASS_Pen_RotateTransform_angle_order_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\rotatetransform_45angle_order.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],RotateTransform method, Pen.RotateTransform, Pen::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_Pen_RotateTransform_angle_order_
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
 - Pen::RotateTransform
 - gdipluspen/Pen::RotateTransform
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
 - Pen.RotateTransform
---

# Pen::RotateTransform


## -description

The <b>Pen::RotateTransform</b> method updates the world transformation matrix of this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object with the product of itself and a rotation matrix.

## -parameters

### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the rotation matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the rotation matrix is on the right. The default value is <b>MatrixOrderPrepend</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-gettransform">Pen::GetTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-multiplytransform">Pen::MultiplyTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-resettransform">Pen::ResetTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-scaletransform">Pen::ScaleTransform</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-settransform">Pen::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>