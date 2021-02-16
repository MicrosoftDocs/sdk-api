---
UID: NF:gdiplusmatrix.Matrix.GetElements
title: Matrix::GetElements (gdiplusmatrix.h)
description: The Matrix::GetElements method gets the elements of this matrix. The elements are placed in an array in the order m11, m12, m21, m22, m31, m32, where mij denotes the element in row i, column j.
helpviewer_keywords: ["GetElements","GetElements method [GDI+]","GetElements method [GDI+]","Matrix class","Matrix class [GDI+]","GetElements method","Matrix.GetElements","Matrix::GetElements","_gdiplus_CLASS_Matrix_GetElements_","gdiplus._gdiplus_CLASS_Matrix_GetElements_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_GetElements_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\getelements.htm
ms.date: 12/05/2018
ms.keywords: GetElements, GetElements method [GDI+], GetElements method [GDI+],Matrix class, Matrix class [GDI+],GetElements method, Matrix.GetElements, Matrix::GetElements, _gdiplus_CLASS_Matrix_GetElements_, gdiplus._gdiplus_CLASS_Matrix_GetElements_
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
 - Matrix::GetElements
 - gdiplusmatrix/Matrix::GetElements
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
 - Matrix.GetElements
---

# Matrix::GetElements


## -description

The <b>Matrix::GetElements</b> method gets the elements of this matrix. The elements are placed in an array in the order m11, m12, m21, m22, m31, m32, where mij denotes the element in row i, column j.

## -parameters

### -param m [out]

Type: <b>REAL*</b>

Pointer to an array that receives the matrix elements. The size of the array should be 6
					×<b>sizeof</b>(
					<b>REAL</b>).

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns OK, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-setelements">Matrix::SetElements</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>