---
UID: NF:gdiplusmatrix.Matrix.Scale
title: Matrix::Scale (gdiplusmatrix.h)
description: The Matrix::Scale method updates this matrix with the product of itself and a scaling matrix.
helpviewer_keywords: ["Matrix class [GDI+]","Scale method","Matrix.Scale","Matrix::Scale","Scale","Scale method [GDI+]","Scale method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_Scale_scaleX_scaleY_order_","gdiplus._gdiplus_CLASS_Matrix_Scale_scaleX_scaleY_order_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Scale_scaleX_scaleY_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\scale.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],Scale method, Matrix.Scale, Matrix::Scale, Scale, Scale method [GDI+], Scale method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Scale_scaleX_scaleY_order_, gdiplus._gdiplus_CLASS_Matrix_Scale_scaleX_scaleY_order_
req.header: gdiplusmatrix.h
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
 - Matrix::Scale
 - gdiplusmatrix/Matrix::Scale
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
 - Matrix.Scale
---

# Matrix::Scale


## -description

The <b>Matrix::Scale</b> method updates this matrix with the product of itself and a scaling matrix.

## -parameters

### -param scaleX [in]

Type: <b>REAL</b>

Real number that specifies the horizontal scale factor.

### -param scaleY [in]

Type: <b>REAL</b>

Real number that specifies the vertical scale factor.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the scaling matrix is on the left, and MatrixOrderAppend specifies that the scaling matrix is on the right. The default value is MatrixOrderPrepend.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply">Matrix::Multiply</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate">Matrix::Rotate</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat">Matrix::RotateAt</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-shear">Matrix::Shear</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-translate">Matrix::Translate</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>