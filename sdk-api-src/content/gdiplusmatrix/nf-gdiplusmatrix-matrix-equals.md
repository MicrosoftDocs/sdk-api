---
UID: NF:gdiplusmatrix.Matrix.Equals
title: Matrix::Equals (gdiplusmatrix.h)
description: The Matrix::Equals method determines whether the elements of this matrix are equal to the elements of another matrix.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","Matrix class","Matrix class [GDI+]","Equals method","Matrix.Equals","Matrix::Equals","_gdiplus_CLASS_Matrix_Equals_matrix_","gdiplus._gdiplus_CLASS_Matrix_Equals_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Equals_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\equals.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Matrix class, Matrix class [GDI+],Equals method, Matrix.Equals, Matrix::Equals, _gdiplus_CLASS_Matrix_Equals_matrix_, gdiplus._gdiplus_CLASS_Matrix_Equals_matrix_
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
 - Matrix::Equals
 - gdiplusmatrix/Matrix::Equals
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
 - Matrix.Equals
---

# Matrix::Equals


## -description

The <b>Matrix::Equals</b> method determines whether the elements of this matrix are equal to the elements of another matrix.

## -parameters

### -param matrix [in]

Type: <b>const Matrix*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that is compared with this 
					<b>Matrix</b> object.

## -returns

Type: <b>BOOL</b>

If the elements of the two matrices are the same, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>